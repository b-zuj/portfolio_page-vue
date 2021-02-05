<template>
  <figure 
    v-for="(element, index) in content"
    v-bind:key="index" 
    class="table__figure"
  >
    <img 
      v-bind:src="logos[`${element.toLowerCase()}`]" 
      v-bind:alt="element" 
      class="figure__img"
    >
    <figcaption class="figure__caption">{{ element }}</figcaption>
  </figure>
</template>

<script>
const aws = require('../assets/logos/aws.png');
const css3 = require('../assets/logos/css3.png');
const eslint = require('../assets/logos/eslint.png');
const express = require('../assets/logos/express.png');
const github = require('../assets/logos/github-black.png');
const heroku = require('../assets/logos/heroku.png');
const html5 = require('../assets/logos/html5.png');
const javascript = require('../assets/logos/javascript.png');
const mocha = require('../assets/logos/mocha.png');
const mongodb = require('../assets/logos/mongodb.png');
const netlify = require('../assets/logos/netlify.png');
const node = require('../assets/logos/node.png');
const postgresql = require('../assets/logos/postgresql.png');
const react = require('../assets/logos/react.png');
const redux = require('../assets/logos/redux.png');
const typescript = require('../assets/logos/typescript.png');
const vue = require('../assets/logos/vue.png');

const logos = {
  'aws': aws,
  'css3': css3,
  'eslint': eslint,
  'express': express,
  'github': github,
  'heroku': heroku,
  'html5': html5,
  'javascript': javascript,
  'mocha': mocha,
  'mongodb': mongodb,
  'netlify': netlify,
  'node': node,
  'postgresql': postgresql,
  'react': react,
  'redux': redux,
  'typescript': typescript,
  'vue': vue
};

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
      logos,
    }
  }
};
</script>

<style scoped>
.table__figure {
  width: 5rem;
  height: 5rem;
  padding: 0.8rem;
  border-style: none;
  border-radius: 5px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin: 0 0.5rem 0.3rem;
}

.table__figure:hover {
  background-color: #0C5887;
}

.figure__img {
  height: 4rem;
}

.figure__caption {
  font-size: 1rem;
  font-weight: 400;
  color: white;
  margin-top: 10px;
}

@media (max-width: 800px) {
  .table__figure {
    margin:0 0.3rem 0.2rem;
  }
}

</style>
