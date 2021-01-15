<template>
  <div v-for="(element, index) in content" v-bind:key="index">
      {{ element }}
      <img v-bind:src="logos[`${element.toLowerCase()}`]" v-bind:alt="element" height="50">
  </div>
</template>

<script>
const aws = require('../assets/logos/aws.png')
const css3 = require('../assets/logos/css3.png')
const eslint = require('../assets/logos/eslint.png')
const express = require('../assets/logos/express.png')
const github = require('../assets/logos/github.png')
const heroku = require('../assets/logos/heroku.png')
const html5 = require('../assets/logos/html5.png')
const javascript = require('../assets/logos/javascript.png')
const linkedin = require('../assets/logos/linkedin.png')
const mocha = require('../assets/logos/mocha.png')
const mongodb = require('../assets/logos/mongodb.png')
const netlify = require('../assets/logos/netlify.png')
const node = require('../assets/logos/node.png')
const postgresql = require('../assets/logos/postgresql.png')
const react = require('../assets/logos/react.png')
const redux = require('../assets/logos/redux.png')
const typescript = require('../assets/logos/typescript.png')
const vue = require('../assets/logos/vue.png')

const logos = {'aws': aws, 'css3': css3, 'eslint': eslint, 'express': express, 'github': github, 'heroku': heroku, 'html5': html5, 'javascript': javascript, 'linkedin': linkedin, 'mocha': mocha, 'mongodb': mongodb, 'netlify': netlify, 'node': node, 'postgresql': postgresql, 'react': react, 'redux': redux, 'typescript': typescript, 'vue': vue}

export default {
  name: 'Logo',
  props: {
    content: {
      type: Object,
      default: () => ({})
    },
  },
  data () {
    return {
      logos
    }
  },
  mounted () { 
      console.log(this.content)
    }
}
</script>

<style>

</style>
