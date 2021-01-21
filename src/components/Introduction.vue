<template>
  <h2>About</h2>
  <table>
    <th colspan="2">
      <img v-bind:src="profile" alt="Barbara Zujewska - profile">
    </th>
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
const profile = require('../assets/profile.jpg');

export default {
  name: 'Introduction',
  components: {
    List,
  },
  props: {
    introduction: {
      type: Object,
      default: () => ({})
    },
    content: {
      type: Object,
      default: () => ({})
    },
  },
  data () {
    return {
      profile,
    }
  }
}
</script>

<style scoped>
h2 {
  /* margin-top: 0.83rem; */
  margin-block-start: 0;
  width: 70%;
  margin: 0.83rem auto 0;
}

img {
  position: absolute;
  height: 15rem;
  border-radius: 50%;
  right: 15%;
  top: 12%;
}

table {
  width: 70%;
  margin-left: auto;
  margin-right: auto;
  font-size: 1rem;
  grid-column-start: 2;
  grid-column-end: five;
  grid-row-start: row1-start;
  grid-row-end: 3;
}

/* table tr {
  border-bottom: thin solid #0C5887;
} */

/* table tr:last-child {
  border: 0;
} */

th {
  text-align: left;
  vertical-align: top;
  font-weight: normal;
}

th.label {
  padding-top: 1.5rem;
  font-weight: 800;
}

th.content {
  margin-left: 3rem;
  padding-top: 1.5rem;
  padding-bottom: 1.5rem;
  padding-left: 6rem;
}

th.list {
  padding-left: 6rem;
}


@media screen and (max-width: 1000px) {
  img {
    position: relative;
    display: block;
    margin: 10px auto 0;
    text-align: center;
    right: auto;
    top: auto;
  }
}

@media screen and (max-width: 800px) {
  
  table {
    width: 90%
  }

  th.label {
    padding-top: 1rem;
  }

  th.content {
    margin-left: 3rem;
    padding-top: 1rem;
    padding-bottom: 1rem;
    padding-left: 3rem;
  }

  th.list {
    /* padding-top: 1rem; */
    padding-left: 3rem;
    
  }
}
</style>
