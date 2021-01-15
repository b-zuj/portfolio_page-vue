<template>
  <img alt="Vue logo" src="./assets/logo.png"> 
  <Welcome heading="Hi, I'm Barbara!" msg="I'm a full stack web developer with keen interest in AI and Big Data."/>
  <Introduction :content="factSheetData" />
  <Skils :content="webTechSkils" />
  <Projects :content="projectsData" />
</template>

<script>
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
      factSheetData: {
        Nationality: 'Polish',
        Residing: 'Oslo, Norway',
        Background: 'industrial management (BEng), marketing and data analytics (Double MSc)',
        'Strong suits': `
          I'm a quick learner with a can-do attitude - tell me what you need and I will figure out how to make it work. 
          Exceptional presentation skills, gained over years of presenting for audiences with various background and knowlege of the subject.
          Unique perspective thanks to the background in management, engineering, and marketing.
          True team player who is not afraid to speak up and take the lead when needed.
          Extensive international communication experience after studying and living in an international environment for over 10 years.
        `,
        'Free time': 'baking, traveling, jigsaw puzzles, obsesssing over my cat',
        },
      projectsData: {
        'Portfolio page': {
          description: 'bla bla',
          tech: 'Vue.js',
          github: '',
          link: '',
        },
        'PhysIO web app': {
          description: 'bla bla',
          tech: 'React, Redux, REST, MongoDB',
          github: '',
          link: '',
        },
        'Baking recipes blog': {
          description: 'bla bla',
          tech: 'React, REST',
          github: '',
          link: '',
        },
        'SPA gallery page': {
          description: 'bla bla',
          tech: 'Vanila JS, REST',
          github: '',
          link: '',
        },
        'ToDo app': {
          description: 'bla bla',
          tech: 'React',
          github: '',
          link: '',
        },
      },
      webTechSkils: {
        languages: ['JavaScript'],
        backend: ['Node', 'Express', 'PostgreSQL', 'MongoDB'],
        frontend: ['HTML5', 'CSS3', 'React', 'Redux'],
        other: ['GitHub'],
      },
      contactLinks: {
        GitHub: '',
        LinkedIn: '',
      },
    }
  }
}
</script>

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
