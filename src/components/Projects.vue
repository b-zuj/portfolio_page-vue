<template>
  <h2>My projects</h2>
  <article v-for="(value, propertyName, index) in content" v-bind:key="index">
    <h3>{{ propertyName }}</h3>
    <p>{{ value.description }}</p>
    <h4>Tech:</h4> <p>{{ value.tech }}</p>
    <a v-if="value.link" v-bind:href="value.link"><img v-bind:src="www" height="20">Project site</a>
    <a v-if="value.github" v-bind:href="value.github"><img v-bind:src="github" height="20">GitHub repo</a>
    <a v-if="value.frontend" v-bind:href="value.frontend"><img v-bind:src="github" height="20">Frontend repo</a>
    <a v-if="value.backend" v-bind:href="value.backend"><img v-bind:src="github" height="20">Backend repo</a>
  </article>
</template>

<script>
const github = require('../assets/logos/github-white.png')
const www = require('../assets/logos/www.png')

export default {
  name: 'Projects',
  props: {
    content: {
      type: Object,
      default: () => ({})
    },
  },
  data () {
    return {
      github,
      www
    }
  },
}
</script>

<style scoped>
article {
  width: 50%;
  padding: 4rem;
  margin-left: auto;
  margin-right: auto;
  font-size: 1rem;
  border-radius: 10px;
  border-width: 0px;
  margin-bottom: 10rem;
  box-shadow: 2px 2px 4px #0C5887;
}

a {
  background-color: #0C5887;
  color: white;
  margin: 10px;

  padding: 1rem 1.5rem;
  text-decoration: none;
  text-transform: uppercase;
  border-radius: 5px;
}

a:hover {
  background-color: #7CC6F4;
}
</style>
