<template>
  <h2>{{ heading }}</h2>
  <p>{{ msg }}</p>
</template>

<script>
export default {
  name: 'Welcome',
  props: {
    heading: String,
    msg: String
  }
}
</script>

<style>

</style>