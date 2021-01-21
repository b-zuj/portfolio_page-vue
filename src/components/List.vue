<template>
  <ul v-for="(value, index) in content" v-bind:key="index">
    <li>{{ value }}</li>
  </ul>
</template>

<script>
export default {
  name: 'List',
  props: {
    content: {
      type: Object,
      default: () => ({})
    },
  }
};
</script>

<style>
ul {
  list-style-type: circle;
  padding-inline-start: 20px;
}

li {
  padding-bottom: 1rem;
}
</style>