<template>
  <div v-for="(element, index) in content" v-bind:key="index">
      <img v-bind:src="`${element.toLowerCase()}.png`" v-bind:alt="element" height="45">
  </div>
</template>

<script>
export default {
  name: 'Logo',
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

