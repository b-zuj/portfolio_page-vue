<template>
  <h2>My projects</h2>
  <article v-for="(value, propertyName, index) in content" v-bind:key="index">
    <h3>{{ propertyName }}</h3>
    <p>{{ value.description }}</p>
    <h4>Tech:</h4> <p>{{ value.tech }}</p>
    <a v-if="value.link" v-bind:href="value.link">Project site</a>
    <a v-if="value.github" v-bind:href="value.github">GitHub repo</a>
    <a v-if="value.frontend" v-bind:href="value.frontend">Frontend repo</a>
    <a v-if="value.backend" v-bind:href="value.backend">Backend repo</a>
  </article>
</template>

<script>
export default {
  name: 'Projects',
  props: {
    content: {
      type: Object,
      default: () => ({})
    },
  },
  mounted () { 
      console.log(this.content)
    }
}
</script>

<style>

</style>
