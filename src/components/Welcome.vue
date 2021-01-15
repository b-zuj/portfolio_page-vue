<template>
  <h2>{{ content.heading }}</h2>
  <p>{{ content.msg }}</p>
</template>

<script>
export default {
  name: 'Welcome',
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