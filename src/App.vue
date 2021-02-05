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
@import url('https://fonts.googleapis.com/css2?family=Ubuntu:ital,wght@0,300;0,400;0,700;1,400&display=swap');

* {
  margin:0;
  padding:0;
  margin-block-start: 0;
  margin-block-end: 0;
}

body {
  font-family: 'Ubuntu', sans-serif;
}

</style>
