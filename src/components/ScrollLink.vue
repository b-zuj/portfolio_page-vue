<template>
  <a class="ul__a" @click="scroll()">{{id}}</a>
</template>

<script>
export default {
  name: "ScrollLink",
  props: ['id'],
  methods: {
    scroll() {
      document.querySelector(`#${this.id}`).scrollIntoView({ behavior: 'smooth' });
    },
  }
}
</script>

<style>

</style>