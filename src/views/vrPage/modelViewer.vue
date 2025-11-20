<template>
  <div id="vr-page">
    <model-viewer
      class="model-viewer"
      src="/threeFile/glb/glb-9.glb"
      ar
      shadow-intensity="1"
      camera-controls
      min-camera-orbit="auto auto 1m"
      max-camera-orbit="auto auto 5m"
      touch-action="pan-y"
    ></model-viewer>
  </div>
</template>
<script setup name="vrPage">
import "@google/model-viewer";
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
