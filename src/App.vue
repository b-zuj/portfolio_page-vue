<template>
  <Welcome  :content="welcomeMsg" />
  <Introduction :content="factSheetData" />
  <Skils :content="webTechSkils" />
  <Projects :content="projectsData" />
</template>

<script>
import jsonData from './assets/data.json'
import Welcome from './components/Welcome.vue'
import Introduction from './components/Introduction.vue'
import Skils from './components/Skils.vue'
import Projects from './components/Projects.vue'


export default {
  name: 'App',
  components: {
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

Vue.config.devtools = true;

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
