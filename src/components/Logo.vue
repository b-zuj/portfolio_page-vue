<template>
  <div v-for="(value, propertyName, index) in content" v-bind:key="index">
    <a v-bind:href="value.link" v-bind:title="propertyName">
      <img v-bind:src="value.logo" v-bind:alt="propertyName" width="30px" height="30px">
    </a>
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