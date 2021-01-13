<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Hello World"/>
  <Welcome msg="Welcome to my portfolio page!"/>
  <Introduction msg="My name is Barbara Zujewska."/>
</template>

<script>
import Welcome from './components/Welcome.vue'
import Introduction from './components/Introduction.vue'

export default {
  name: 'App',
  components: {
    Welcome,
    Introduction
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
