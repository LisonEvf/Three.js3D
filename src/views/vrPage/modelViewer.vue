<template>
  <div id="vr-page">
    <model-viewer
      class="model-viewer"
      :src="modelSrc"
      ar
      shadow-intensity="1"
      camera-controls
      min-camera-orbit="auto auto 0m"
      max-camera-orbit="auto auto 5m"
      touch-action="pan-y"
      scale="0.5 0.5 0.5"
    ></model-viewer>
  </div>
</template>
<script setup name="vrPage">
import "@google/model-viewer";

const modelSrc = `${import.meta.env.BASE_URL}threeFile/glb/glb-7.glb`;
</script>
<style lang="scss" scoped>
#vr-page {
  position: relative;
  width: 100%;
  height: 100vh;
}
.model-viewer {
  width: 100%;
  height: 100%;
}
</style>
