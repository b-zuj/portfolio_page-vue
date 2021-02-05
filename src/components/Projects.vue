<template>
  <h2 class="section__h2">Projects</h2>
  <div class="grid">
    <div v-for="(value, propertyName, index) in content" v-bind:key="index" class="project">
      <div class="name">
        <h4>{{ propertyName }}</h4>
      </div>
      <div class="details">
        <p>{{ value.description }}</p>
        <div class="tech">
          <h5>Tech:</h5>
          <p>{{ value.tech }}</p>
        </div>
        <a v-if="value.link" v-bind:href="value.link"><img v-bind:src="www" height="20">Project site</a>
        <a v-if="value.github" v-bind:href="value.github"><img v-bind:src="github" height="20">GitHub repo</a>
        <a v-if="value.frontend" v-bind:href="value.frontend"><img v-bind:src="github" height="20">Frontend repo</a>
        <a v-if="value.backend" v-bind:href="value.backend"><img v-bind:src="github" height="20">Backend repo</a>
      </div>
    </div>
  </div>
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
.grid {
  width: 100%;
  display: inline-grid;
  grid-template-columns: 10% auto 10%;
  grid-template-rows: auto;
  justify-items: center;
}

.project {
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

.name {
	background-color: #083D5E;
	color: #fff;
	padding: 20px;
	width: 200px;
}

.details {
	padding: 20px;
	position: relative;
	width: 100%;
  text-align: start;
}

.details p {
  margin-block-start: 0;
}

.tech h5,
.tech p {
  display: inline;
  vertical-align: top;
  font-size: 16px;
  line-height: 28px;
  text-align: start;
}

.tech h5 {
  padding-right: 15px;
}

a {
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

a:hover {
  background-color: #7CC6F4;
  color: #0C5887;
}

img {
  margin-right: 7px;
}

@media screen and (max-width: 720px) {
  .grid {
    grid-template-columns: 5% auto 5%;
  }

  .project {
    flex-direction: column;
    min-width: 350px;
  }

  .name {
    padding: 0;
    width: 100%;
  }

  .details {
    padding: 10px;
    position: relative;
    width: auto;
    text-align: start;
  }
}
</style>
