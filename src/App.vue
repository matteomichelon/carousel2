<template>
  <div id="app">
    <Slider />
  </div>
</template>

<script>
import Slider from "./components/Slider.vue";

export default {
  name: "App",
  components: {
    Slider,
  },
};
</script>

<style lang="scss">
html {
  font: 12px Tahoma, Geneva, sans-serif;
}

* {
  margin: 0;
  padding: 0;
  //color: #fff;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

img{
  width: 100%;
  height: auto;
}
</style>
