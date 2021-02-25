<template>
<<<<<<< HEAD:src/components/Tools.vue
<section class="main__section main__section--tools" id="Tools">
  <h2 class="section__h2">Preferred web development tools</h2>
  <table class="section__table">
    <tr class="table__tr" v-for="(value, propertyName, index) in content" v-bind:key="index">
      <th class="tr__th">
=======
  <h2>Preferred web development tools</h2>
  <table>
    <tr v-for="(value, propertyName, index) in content" v-bind:key="index">
      <th>
>>>>>>> 94de7f8af6a481169c8473e24920d7d0c586688a:src/components/Skils.vue
        <Logo :content="value" />
      </th>
    </tr>
  </table>
</section>
</template>

<script>
import Logo from './Logo.vue';

export default {
  name: 'Tools',
  components: {
    Logo,
  },
  props: {
    content: {
      type: Object,
      default: () => ({})
    },
  }
};
</script>

<style scoped>
.section__table {
  margin: 30px 0 0;
  display: flex;
  flex-direction: column;
}

.tr__th {
  display: flex;
  flex-flow: wrap;
  justify-content: center;
  margin-bottom: 0.5rem;
}
</style>
