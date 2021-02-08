<template>
  
  <Navigation />
  <div class="parallax" id="parallax">
  
    <div class="parallax__layer parallax__layer--1" id="keyart-0"></div>
    <div class="parallax__layer parallax__layer--2" id="keyart-1"></div>
    <div class="parallax__layer parallax__layer--3" id="keyart-2"></div>
    <div class="parallax__layer parallax__layer--4" id="keyart-3"></div>
    <div class="parallax__layer parallax__layer--5" id="keyart-4"></div>
    <div class="parallax__layer parallax__layer--6" id="keyart-5"></div>
    <div class="parallax__layer parallax__layer--7" id="keyart-6"></div>
    <div class="parallax__layer parallax__layer--8" id="keyart-7"></div>
    <div class="parallax__layer parallax__layer--9" id="keyart-8"></div>

    
    <Header :content="welcomeMsg" />
    
    <main class="main">
      <About :content="factSheetData" />
      <Tools :content="webTechSkils" />
      <Projects :content="projectsData" />
      <Footer :content="contactLinks" />
    </main>
  
  </div>

  

</template>

<script>
import Navigation from './Navigation.vue'
import Header from './Header.vue';
import About from './About.vue';
import Tools from './Tools.vue';
import Projects from './Projects.vue';
import Footer from './Footer.vue';

export default {
  name: 'Parallax',
  components: {
    Navigation,
    Header,
    About,
    Tools,
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
    }
  },
};
</script>

<style>
.parallax {
  height: 100vh;
  overflow-x: hidden;
  overflow-y: auto;
  -webkit-perspective: 1px;
  perspective: 1px;
}

.parallax__layer {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-position: bottom center;
  background-size: 100%;
  background-repeat: no-repeat;
}

.parallax__layer--1 {
  -webkit-transform: translateZ(-15px) scale(16);
  transform: translateZ(-15px) scale(16);
  background-image: url('../assets/parallax/1.png');
  background-color: #D4ECFA;
}

.parallax__layer--2 {
  -webkit-transform: translateZ(-12px) scale(13);
  transform: translateZ(-12px) scale(13);
  background-image: url('../assets/parallax/2.png');
}

.parallax__layer--3 {
  -webkit-transform: translateZ(-10px) scale(11);
  transform: translateZ(-10px) scale(11);
  background-image: url('../assets/parallax/3.png');
}

.parallax__layer--4 {
  -webkit-transform: translateZ(-8px) scale(9);
  transform: translateZ(-8px) scale(9);
  background-image: url('../assets/parallax/4.png');
}

.parallax__layer--5 {
  -webkit-transform: translateZ(-6px) scale(7);
  transform: translateZ(-6px) scale(7);
  background-image: url('../assets/parallax/5.png');
}

.parallax__layer--6 {
  -webkit-transform: translateZ(-4px) scale(5);
  transform: translateZ(-4px) scale(5);
  background-image: url('../assets/parallax/6.png');
}

.parallax__layer--7 {
  -webkit-transform: translateZ(-2px) scale(3);
  transform: translateZ(-2px) scale(3);
  background-image: url('../assets/parallax/7.png');
}

.parallax__layer--8 {
  -webkit-transform: translateZ(-1px) scale(2);
  transform: translateZ(-1px) scale(2);
  background-image: url('../assets/parallax/8.png');
}

.parallax__layer--9 {
  -webkit-transform: translateZ(0px);
  transform: translateZ(0px);
  background-image: url('../assets/parallax/9.png');
}

.main {
  position: absolute;
  margin-top: 100vh;
  width: 100%;
  display: block;
  background-color: white;
}

.main__section {
  width: 80%;
  max-width: 1100px;
  margin: 10vh auto 0;
  padding-top: 70px;
}

.section__h2 {
  font-size: 2.2rem;
  margin: 0 auto 0;
}

</style>