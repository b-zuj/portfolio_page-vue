<template>
  <table>
    <tr v-for="(value, propertyName, index) in content" v-bind:key="index">
      <th>{{ propertyName }}:</th>
      <th v-if="Array.isArray(value)">
        <List :content="value" />
      </th>
      <th v-else>{{ value }}</th>
    </tr>
  </table>
  <!-- <p>{{ content }}</p> -->
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
      for (const [key, value] of Object.entries(this.content)) {
        console.log(typeof value);
        console.log(key);
    }
  }
}
</script>

<style>

</style>