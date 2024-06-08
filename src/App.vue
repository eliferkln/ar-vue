<template>
  <div id="app">
    <div class="model">
      <div class="model__view">
        <model-viewer
          id="first"
          src="/assets/mickey.glb"
          ios-src="/assets/mickey.usdz"
          seamless-poster
          environment-image="neutral"
          exposure="1.0"
          interaction-prompt-threshold="0"
          shadow-intensity="1"
          ar
          autoplay
          ar-modes="webxr scene-viewer quick-look"
          auto-rotate
          camera-controls
          camera-orbit="0deg 90deg 0deg 8.37364m"
          alt="3D model"
          style="
            display: flex;
            align-items: center;
            background-color: transparent;
            margin: auto;
          "
        ></model-viewer>
      </div>
    </div>
  </div>
</template>

<script>
import '@google/model-viewer'
export default {
  name: 'App',
}
</script>

<style scoped>
.model {
  margin-top: 35px;
}
.model__view model-viewer {
  width: 20em;
  height: 20em;
}
@media only screen and (min-width: 320px) and (max-width: 480px) {
  .model__view model-viewer {
    width: 15em;
    height: 15em;
  }
}
</style>
