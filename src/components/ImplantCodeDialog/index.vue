<template>
	<el-dialog v-model="visible" title="将当前编辑效果嵌入你的项目" width="600px" :close-on-click-modal="false">
		<el-scrollbar max-height="400px">
			<code class="code">{{ codeIframe }}</code>
		</el-scrollbar>
		<el-row :style="{ marginTop: '10px' }">
			<el-col :span="12">
				<el-text type="primary">容器宽度</el-text>
				<el-input-number class="number-style" :precision="0" v-model="iframeConfig.width" />
			</el-col>
			<el-col :span="12">
				<el-text type="primary">容器高度</el-text>
				<el-input-number class="number-style" :precision="0" v-model="iframeConfig.height" />
			</el-col>
		</el-row>
		<template #footer>
			<span class="dialog-footer">
				<el-button type="primary" class="copy-button" @click="onCopyCode">
					复制代码
				</el-button>
			</span>
		</template>
	</el-dialog>
</template>
<script setup lang="ts">
import { ElMessage } from "element-plus";
import { defineExpose, ref, Ref, reactive, computed } from 'vue'
import { pageEnums } from '@/enums/pageEnums'
import Clipboard from 'clipboard';

const visible: Ref<boolean> = ref(false)
const codeString: Ref<any> = ref(null)
const iframeConfig = reactive({
	width: 400,
	height: 300,
})

const codeIframe = computed(() => {
	const codeConfig = codeString.value.replace(/"([^"\\]*(\\.[^"\\]*)*)"/g, "'$1'");
	const src = `${pageEnums.MODEL_PREIVEW}?` + 'modelConfig=' + codeConfig
	const iframe = `<iframe  width="${iframeConfig.width}" height="${iframeConfig.height}" src="${src}" allowfullscreen></iframe>`;
	return iframe
})

const showDialog = (code: string) => {
	visible.value = true
	codeString.value = JSON.stringify(code)
}

const onCopyCode = () => {
	const clipboard = new Clipboard('.copy-button', { text: () => codeIframe.value });
	clipboard.on('success', (val) => {
		ElMessage.success('复制成功,将代码粘贴至你的项目中即可')
		clipboard.destroy();
		visible.value = false
	});
	clipboard.on('error', () => {
		console.log('复制失败');
		clipboard.destroy();
	});
}

defineExpose({ showDialog })
</script>


<style lang="scss" scoped>
.code {
	display: block;
	background-color: #f9f9f9;
	padding: 10px;
	font-family: Consolas, monospace;
	color: #333;
	word-wrap: break-word;
}

.number-style {
	width: 150px !important;
}
</style>


