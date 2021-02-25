<template>
  <a @click="scroll()">{{id}}</a>
</template>

<script>
export default {
  name: "ScrollLink",
  props: ['id'],
  methods: {
    scroll() {
      if (this.id === 'BZuj' || this.id === 'Barbara Zujewska') {
        document.querySelector(`#keyart-8`).scrollIntoView( { alignTo: true, behavior: 'smooth' });
        return;
      }
      document.querySelector(`#${this.id}`).scrollIntoView({ behavior: 'smooth' });
    },
  }
}
</script>
