<template>
  <header class="header">
    <h1 class="header__h1">{{content.msg1}}</h1>
    <h2 class="header__h2">{{content.msg2}}</h2>
  </header>
</template>

<script>
export default {
  name: 'Header',
  props: {
    content: {
      type: Object,
      default: () => ({})
    },
  },
  mounted(){
    console.log(this.content)
  }
}
</script>

<style>

.header {
  display: block;
  position: absolute;
  bottom: 5%;
  left: 10%;
  right: 10%
}

.header__h1 {
  margin-bottom: 10px;
}
</style>