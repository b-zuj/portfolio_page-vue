<template>
  <h1>{{ content.heading }}</h1>
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
