<template>
  <Parallax :content="jsonData" />

</template>

<script>
import jsonData from './assets/data.json';
import Parallax from './components/Parallax.vue';

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
};
</script>

<style>
html, body, div, span, applet, object, iframe, blockquote, pre,
abbr, acronym, address, big, cite, code,
del, dfn, em, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,dl, dt, dd, ol,
fieldset, form, label, legend,
caption, tbody, tfoot, thead, aside, canvas, details, embed, 
figure, figcaption, header, hgroup, 
menu, nav, output, ruby, summary,
time, mark, audio, video {
	margin: 0;
	padding: 0;
	border: 0;
	font-size: 100%;
	vertical-align: baseline;
}

body {
	line-height: 1;
}

table {
	border-collapse: collapse;
	border-spacing: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

</style>
