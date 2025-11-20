<template>
  <div id="vr-page">
    <el-button @click="createAR" type="primary">打开AR</el-button>
  </div>
</template>
<script setup>
import { activateAR } from "@/utils/utilityFunction";
const createAR = () => {
  activateAR({
    iosSrc: "https://three3d-0gte3eg619c78ffd-1301256746.tcloudbaseapp.com/2025_11_20 17_05_55.usdz"
  });
};
</script>

<style lang="scss" scoped>
#vr-page {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
