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

@media only screen and (min-width: 768px) and (max-width: 1100px) {
  .header {
    bottom: 2%;
  }

  .header__h1 {
    margin-bottom: 5px;
  }
}
</style>