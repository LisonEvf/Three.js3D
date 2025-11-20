<template>
  <el-config-provider>
    <router-view />
    <MessageTipDialog ref="messageTipDialog" />
  </el-config-provider>
</template>
<script setup>

import MessageTipDialog from "@/components/MessageTipDialog/index.vue";


</script>
