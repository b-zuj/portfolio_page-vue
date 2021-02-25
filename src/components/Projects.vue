<template>
<section class="main__section main__section--projects" id="Projects">
  <h2 class="section__h2">Projects</h2>
  <div class="section__div--grid">
    <div v-for="(value, propertyName, index) in content" v-bind:key="index" class="grid__div--project">
      <div class="project__div--name">
        <h4 class="project__h4">{{ propertyName }}</h4>
      </div>
      <div class="project__div--details">
        <p class="details__p--description">{{ value.description }}</p>
        <div class="details__div--tech">
          <h5 class="tech__h5">Tech:</h5>
          <p class="tech__p">{{ value.tech }}</p>
        </div>
        <a class="details__a" v-if="value.link" v-bind:href="value.link"><img v-bind:src="www" height="20">Project site</a>
        <a class="details__a" v-if="value.github" v-bind:href="value.github"><img v-bind:src="github" height="20">GitHub repo</a>
        <a class="details__a" v-if="value.frontend" v-bind:href="value.frontend"><img v-bind:src="github" height="20">Frontend repo</a>
        <a class="details__a" v-if="value.backend" v-bind:href="value.backend"><img v-bind:src="github" height="20">Backend repo</a>
      </div>
    </div>
  </div>
</section>
</template>

<script>
const github = require('../assets/logos/github-white.png');
const www = require('../assets/logos/www.png');

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
      www,
    }
  },
};
</script>

<style scoped>
.section__div--grid {
  width: 100%;
  display: inline-grid;
  grid-template-columns: 10% auto 10%;
  grid-template-rows: auto;
  justify-items: center;
}

.grid__div--project {
  grid-column-start: 2;
  grid-column-end: 2;
	background-color: #fff;
	border-radius: 10px;
	box-shadow: 0 10px 10px rgba(12, 88, 135, 0.2);
	display: flex;
	max-width: 100%;
	margin: 20px 0;
	overflow: hidden;
	min-width: 600px;
  max-width: 700px;
}

.project__div--name {
	background-color: #083D5E;
	color: #fff;
	padding: 20px;
	width: 200px;
}

.project__div--details {
	padding: 20px;
	position: relative;
	width: 100%;
  text-align: start;
}

.details__p--description {
  margin-block-start: 0;
}

.tech__h5,
.tech__p {
  display: inline;
  vertical-align: top;
  font-size: 16px;
  line-height: 28px;
  text-align: start;
}

.tech__h5 {
  padding-right: 15px;
}

.details__a {
  display: block;
  float: right;
  background-color: #0C5887;
  color: white;
  margin: 5px;
  font-size: small;
  padding: 7px 7px;
  text-decoration: none;
  text-transform: uppercase;
  border-radius: 5px;
  display: flex;
  align-items: center;
  justify-content: center
}

.details__a:hover {
  background-color: #7CC6F4;
  color: #0C5887;
}

img {
  margin-right: 7px;
}

@media screen and (max-width: 720px) {
  .section__div--grid  {
    grid-template-columns: 3% auto 3%;
  }

  .grid__div--project {
    flex-direction: column;
    min-width: 400px;
  }

  .project__div--name {
    padding: 10px;
    width: 100%;
  }

  .project__div--details {
    padding: 10px;
    position: relative;
    width: auto;
    text-align: start;
  }
}

@media screen and (max-width: 450px) {

  .grid__div--project {
    flex-direction: column;
    min-width: 350px;
  }
}
</style>
