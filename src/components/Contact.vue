<template>
  <h2>Contact</h2>
  <article v-for="(value, propertyName, index) in content" v-bind:key="index">
    <a v-if="propertyName === 'GitHub'" v-bind:href="value.email"><img v-bind:src="email" height="40">barbara@zujewska.com</a>
    <br>
    <a v-if="propertyName === 'GitHub'" v-bind:href="value"><img v-bind:src="github" height="40">{{ propertyName }}</a>
    <a v-if="propertyName === 'LinkedIn'" v-bind:href="value"><img v-bind:src="linkedin" height="40">{{ propertyName }}</a>
  </article>
</template>

<script>
const github = require('../assets/logos/github-black.png');
const linkedin = require('../assets/logos/linkedin.png');
const email = require('../assets/logos/email.png');


export default {
  name: 'Contact',
  props: {
    content: {
      type: Object,
      default: () => ({})
    },
  },
  data () {
    return {
      github,
      email,
      linkedin,
    }
  },
  mounted () {
    console.log(this.content);
  }
};
</script>

<style>

</style>