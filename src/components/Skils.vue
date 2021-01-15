<template>
  <h3>Web development tools:</h3>
  <table>
    <tr v-for="(value, propertyName, index) in content" v-bind:key="index">
      <th>{{ propertyName }}:</th>
      <th v-if="typeof value === 'object'">
        <div v-for="(element, elementName, index) in value" v-bind:key="index">
          <a v-bind:href="element.link" v-bind:title="elementName">
            <img v-bind:src="element.logo" v-bind:alt="elementName" width="30" height="30">
          </a>
        </div>
      </th>
    </tr>
  </table>
</template>

<script>
// import Logo from './Logo.vue'

export default {
  name: 'Skils',
  // components: {
  //   Logo
  // },
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