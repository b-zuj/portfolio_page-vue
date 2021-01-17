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

<style scoped>
h1, p {
  position: absolute;
  left: 0;
  right: 0;
  z-index: 5;
  color: #C3E5FA;
  margin-left: auto;
  margin-right: auto;
  text-align: center;
}

h1 {
  margin-top: 260px;
  
}

p {
  margin-top: 368px;
}

</style>
