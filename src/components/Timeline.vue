<template>
  <p>{{ content }}</p>
</template>

<script>
export default {
  name: 'Timeline',
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