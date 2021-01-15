<template>
  <h2>Fact sheet</h2>
  <table>
    <tr v-for="(value, propertyName, index) in content" v-bind:key="index">
      <th>{{ propertyName }}:</th>
      <th v-if="Array.isArray(value)">
        <List :content="value" />
      </th>
      <th v-else>{{ value }}</th>
    </tr>
  </table>
</template>

<script>
import List from './List.vue'

export default {
  name: 'Introduction',
  components: {
    List
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

</style>
