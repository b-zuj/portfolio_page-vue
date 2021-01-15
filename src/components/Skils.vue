<template>
  <h2>My web development tools</h2>
  <table>
    <tr v-for="(value, propertyName, index) in content" v-bind:key="index">
      <th>{{ propertyName }}:</th>
      <th>
        <Logo :content="value" />
      </th>
    </tr>
  </table>
</template>

<script>
import Logo from './Logo.vue'

export default {
  name: 'Skils',
  components: {
    Logo
  },
  
  props: {
    content: {
      type: Object,
      default: () => ({})
    },
  },
  mounted () { 
      console.log(this.content)
    }
}
</script>

<style>

</style>
