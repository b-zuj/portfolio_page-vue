<template>
  <img class="background" v-bind:src="background">
  <div class="contact">
    <h4 class="header">Contact me: </h4>
    <div v-for="(value, propertyName, index) in content" v-bind:key="index" class="icons">
      <a v-if="propertyName === 'email'" v-bind:href="`mailto:${value}`"><img v-bind:src="email" height="40"></a>
      <a v-if="propertyName === 'GitHub'" v-bind:href="value"><img v-bind:src="github" height="40"></a>
      <a v-if="propertyName === 'LinkedIn'" v-bind:href="value"><img v-bind:src="linkedin" height="40"></a>
    </div>
  </div>
</template>

<script>
const background = require('../assets/footer.png');

const github = require('../assets/logos/github-white.png');
const linkedin = require('../assets/logos/linkedin-white.png');
const email = require('../assets/logos/email-white.png');

export default {
  name: 'Footer',
  props: {
    content: {
      type: Object,
      default: () => ({})
    },
  },
  data () {
    return {
      background,
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

<style scoped>
.background {
  background-color: white;
  margin-bottom: -100px;
  width: 100%;
}

.contact {
  position: absolute;
  width: 100%;
  padding-bottom: 20px;
  padding-top: 10px;
  /* margin-top: -10px; */
  background-color: #083D5E;
}

.header {
  color: white;
  display: inline;
  vertical-align: middle;
  font-size: 20px;
  line-height: 28px;
  margin: 20px;
}

.icons {
  display: inline;
  vertical-align: top;
  font-size: 16px;
  line-height: 28px;
  margin: 20px;
  padding-bottom: 20px;
}
  
</style>