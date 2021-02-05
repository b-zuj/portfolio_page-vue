<template>
  <h2 class="section__h2">Prefered web development tools</h2>
  <table class="section__table">
    <tr class="table__tr" v-for="(value, propertyName, index) in content" v-bind:key="index">
      <th class="tr__th">
        <Logo :content="value" />
      </th>
    </tr>
  </table>
</template>

<script>
import Logo from './Logo.vue';

export default {
  name: 'Skils',
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
