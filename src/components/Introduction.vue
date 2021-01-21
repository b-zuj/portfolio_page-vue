<template>
  <h2>Fact sheet</h2>
  <table>
    <tr v-for="(value, propertyName, index) in content" v-bind:key="index">
      <th class="label">{{ propertyName }}:</th>
      <th v-if="Array.isArray(value)" class="list">
        <List :content="value" />
      </th>
      <th v-else class="content">{{ value }}</th>
    </tr>
  </table>
</template>

<script>
import List from './List.vue';

export default {
  name: 'Introduction',
  components: {
    List,
  },
  props: {
    content: {
      type: Object,
      default: () => ({})
    },
  },
  mounted () { 
    console.log('Introduction received content');
  }
}
</script>

<style>
h2 {
  margin-top: 0.83em;
  margin-block-start: 0;
}

table {
  width: 70%;
  margin-left: auto;
  margin-right: auto;
  font-size: 1rem;
}

th.label {
  padding-top: 1.5rem;
}

th.content {
  margin-left: 3rem;
  padding-top: 1.5rem;
  padding-bottom: 1.5rem;
  padding-left: 6rem;
}

th.list {
  padding-top: 1.5rem;
  padding-left: 6rem;
}

th {
  text-align: left;
  vertical-align: top;
}
</style>
