<template>
  <nav>

  </nav>
  
  <div class="keyart" id="nonparallax"></div>
  <div class="keyart" id="parallax">
    <div class="keyart_layer parallax" id="keyart-0" data-speed="12" style="transform: translateZ(-7px)"></div>
    <div class="keyart_layer parallax" id="keyart-1" data-speed="18" style="transform: translateZ(-6px)"></div>
    <div class="keyart_layer parallax" id="keyart-2" data-speed="26" style="transform: translateZ(-5px)"></div>
    <div class="keyart_layer parallax" id="keyart-3" data-speed="36" style="transform: translateZ(-4px)"></div>
    <div class="keyart_layer parallax" id="keyart-4" data-speed="48" style="transform: translateZ(-3px)"></div>
    <div class="keyart_layer parallax" id="keyart-5" data-speed="58" style="transform: translateZ(-2px)"></div>
    <div class="keyart_layer parallax" id="keyart-6" data-speed="60" style="transform: translateZ(-1px)"></div>
    <img class="keyart_layer parallax" v-bind:src="background" id="keyart-7" data-speed="69" style="transform: translateZ(0px)"/>
    <div class="keyart_layer" id="keyart-8" data-speed="100"><h3>{{ welcomeMsg.msg }}</h3></div>	
    
  </div>


  <main id="maincontain">
    <section class="introduction section">
      <Introduction :content="factSheetData" />
    </section>
    <section class="skills section">
      <Skils :content="webTechSkils" />
    </section>
    <section class="projects section">
      <Projects :content="projectsData" />
    </section>
    <footer class="">
        <Footer :content="contactLinks" />
    </footer>
  </main>
  
</template>

<script>

import Introduction from './Introduction.vue';
import Skils from './Skils.vue';
import Projects from './Projects.vue';
import Footer from './Footer.vue';
const background = require('../assets/parallax/8-skyline.png');

export default {
  name: 'Parallax',
  components: {
    Introduction,
    Skils,
    Projects,
    Footer,
  },
  props: {
    content: {
      type: Object,
      default: () => ({})
    },
  },
  data() {
    return {
      welcomeMsg: this.content.data.welcomeMsg,
      factSheetData: this.content.data.factSheetData,
      projectsData: this.content.data.projectsData,
      webTechSkils: this.content.data.webTechSkils,
      contactLinks: this.content.data.contactLinks,
      background,
    }
  },
};
</script>

<style>
@import '../css/styles.css';
@import url('https://fonts.googleapis.com/css2?family=Neucha&display=swap');

h1, h2, h3, h4 {
  font-family: 'Neucha', cursive;
}

h2 {
  font-size: 2rem;
}

h3 {
  
  text-align: left;
  margin-block-start: 0em;
  margin-block-end: 0em;
  position: absolute;
  bottom: 10%;
  left: 5%;
}

h4 {
  font-size: 1.5rem;
}


section {
  padding-top: 10vh;
  position: relative;
  width: 100%;
  background-color: #ffffff;
}

.section {
  padding-top: 10vh;
  padding-bottom: 5vh;
}

</style>