<template>


  <section class="parallax">
    <Parallax :content="jsonData" />
  </section>



</template>

<script>
import jsonData from './assets/data.json'
import Parallax from './components/Parallax.vue'


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
/* http://meyerweb.com/eric/tools/css/reset/ 
   v2.0 | 20110126
   License: none (public domain)
*/

html, body, div, span, applet, object, iframe, blockquote, pre,
abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol,
fieldset, form, label, legend,
caption, tbody, tfoot, thead, aside, canvas, details, embed, 
figure, figcaption, footer, header, hgroup, 
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
	margin: 0;
	padding: 0;
	border: 0;
	font-size: 100%;
	vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure, 
footer, header, hgroup, menu, nav, section {
	display: block;
}
body {
	line-height: 1;
}
blockquote, q {
	quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
	content: '';
	content: none;
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
  /* background-color: #C3E5FA; */
}



/* section.parallax {
  background-image: url(https://s3.eu-west-1.amazonaws.com/mundy.assets.d3r.com/images/hero_large/62475-northern-lights-cruises-lofoten-norway.jpg);
  background-size: cover;
  background-position: 0 -110px;
} */
</style>
