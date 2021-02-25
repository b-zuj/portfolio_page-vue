<template>
<footer class="main__footer" id="Contact">
  <img class="footer__img" v-bind:src="background">
  <div class="footer__div--content">
    <div class="content__div--contact">
      <h4 class="contact__header">Contact me: </h4>
      <div v-for="(value, propertyName, index) in content" v-bind:key="index" class="contact__div--icons">
        <a class="icons__a" v-if="propertyName === 'email'" v-bind:href="`mailto:${value}`"><img class="icons__img" v-bind:src="email" height="40"></a>
        <a class="icons__a" v-if="propertyName === 'GitHub'" v-bind:href="value"><img class="icons__img" v-bind:src="github" height="40"></a>
        <a class="icons__a" v-if="propertyName === 'LinkedIn'" v-bind:href="value"><img class="icons__img" v-bind:src="linkedin" height="40"></a>
      </div>
    </div>
    <div class="content__div--copyrights">
      <p>Copyright © 2021 - Barbara Zujewska</p>
    </div>
  </div>
</footer>
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
  }
};
</script>

<style scoped>
.footer__img {
  background-color: white;
  margin-bottom: -10px;
  width: 100%;
}

.footer__div--content {
  position: absolute;
  width: 100%;
  padding: 0 0 5%; 
  background-color: #083D5E;
}

.content__div--contact {
  float: right;
  margin-right: 5%;
  padding-bottom: 20px;
}

.contact__header {
  color: white;
  display: inline;
  vertical-align: middle;
  font-size: 20px;
  line-height: 28px;
  margin: 20px;
}

.contact__div--icons {
  display: inline;
  vertical-align: top;
  font-size: 16px;
  line-height: 28px;
  margin: 20px 20px 30px 20px;
}

.content__div--copyrights{
  color: white;
  position: absolute;
  /* margin-left: auto;
  margin-right: auto; */
  margin: 0 auto;
  left: 0;
  right: 0;
  text-align: center;
  bottom: 20px;
}
  
</style>