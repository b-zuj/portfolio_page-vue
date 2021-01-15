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
  },
  mounted () { 
      console.log('List received content')
    }
}
</script>

<style>

</style>