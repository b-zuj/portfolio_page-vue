<template>
  <div class="keyart" id="parallax">
    <div class="keyart_layer parallax" id="keyart-0" data-speed="2" style="transform: translate3d(0px, 0px, 0px)"></div>		<!-- 00.0 -->
    <div class="keyart_layer parallax" id="keyart-1" data-speed="5" style="transform: translate3d(0px, 0px, 0px)"></div>	<!-- 12.5 -->
    <div class="keyart_layer parallax" id="keyart-2" data-speed="11" style="transform: translate3d(0px, 0px, 0px)"></div>		<!-- 25.0 -->
    <div class="keyart_layer parallax" id="keyart-3" data-speed="16" style="transform: translate3d(0px, 0px, 0px)"></div>	<!-- 37.5 -->
    <div class="keyart_layer parallax" id="keyart-4" data-speed="26" style="transform: translate3d(0px, 0px, 0px)"></div>		<!-- 50.0 -->
    <div class="keyart_layer parallax" id="keyart-5" data-speed="36" style="transform: translate3d(0px, 0px, 0px)"></div>	<!-- 62.5 -->
    <div class="keyart_layer parallax" id="keyart-6" data-speed="49" style="transform: translate3d(0px, 0px, 0px)"></div>		<!-- 75.0 -->
    <div class="keyart_layer" id="keyart-scrim"></div>
    <div class="keyart_layer parallax" id="keyart-7" data-speed="69" style="transform: translate3d(0px, 0px, 0px)"></div>		<!-- 87.5 -->
    <div class="keyart_layer" id="keyart-8" data-speed="100"></div>		<!-- 100. -->
  </div>
  <section class="introduction fullpage">
    <Introduction :content="factSheetData" />
  </section>
  <section class="skills fullpage">
    <Skils :content="webTechSkils" />
  </section>
  <section class="projects fullpage">
    <Projects :content="projectsData" />
  </section>
  <footer class="">
    <Contact :content="contactLinks" />
  </footer>
</template>

<script>

import Introduction from './Introduction.vue';
import Skils from './Skils.vue';
import Projects from './Projects.vue';
import Contact from './Contact.vue';

export default {
  name: 'Parallax',
  components: {
    Introduction,
    Skils,
    Projects,
    Contact,
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
    }
  },
};
</script>

<style>
@import './styles.css';

</style>