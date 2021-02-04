<template>
  <Parallax :content="jsonData" />
</template>

<script>
import Parallax from './components/Parallax.vue'
import jsonData from './assets/data.json';

export default {
  name: 'App',
  components: {
    Parallax
  },
  data() {
    return {
      jsonData,
    }
  },
}
</script>

<style>
  * {
    margin:0;
    padding:0;
    margin-block-start: 0;
    margin-block-end: 0;
  }

  body {
    font: 100% / 1.5 Arial;
  }

   /* centre the content in the parallax layers */
  /* .page {
    position: absolute;
    left: 50%;
    top: 50%;
    -webkit-transform: translate(-50%, -50%);
    transform: translate(-50%, -50%);
  } */
</style>
