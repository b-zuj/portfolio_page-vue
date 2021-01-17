<template>


  <section class="parallax">
    <Parallax />
  </section>

  <section>
    <Welcome :content="welcomeMsg" />
  </section>

  <section>
    <Introduction :content="factSheetData" />
  </section>
  <section>
    <Skils :content="webTechSkils" />
  </section>
  <section>
    <Projects :content="projectsData" />
  </section>
  <section>
    contacts?
  </section>

</template>

<script>
import jsonData from './assets/data.json'
import Parallax from './components/Parallax.vue'
import Welcome from './components/Welcome.vue'
import Introduction from './components/Introduction.vue'
import Skils from './components/Skils.vue'
import Projects from './components/Projects.vue'

export default {
  name: 'App',
  components: {
    Parallax,
    Welcome,
    Introduction,
    Skils,
    Projects
  },
  data() {
    return {
      welcomeMsg: jsonData.data.welcomeMsg,
      factSheetData: jsonData.data.factSheetData,
      projectsData: jsonData.data.projectsData,
      webTechSkils: jsonData.data.webTechSkils,
      contactLinks: jsonData.data.contactLinks,
    }
  },
  mounted () {
    console.log(jsonData.data.welcomeMsg)
  }
}
</script>

<style>
/* http://meyerweb.com/eric/tools/css/reset/ 
   v2.0 | 20110126
   License: none (public domain)
*/

html, body, div, span, applet, object, iframe, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed, 
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
ol, ul {
	list-style: none;
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

section {
  /* height: 120%; */
  min-height: 100vh;
  width: 100%;
}

/* section.parallax {
  background-image: url(https://s3.eu-west-1.amazonaws.com/mundy.assets.d3r.com/images/hero_large/62475-northern-lights-cruises-lofoten-norway.jpg);
  background-size: cover;
  background-position: 0 -110px;
} */
</style>
