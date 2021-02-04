<template>
  <h2 class="section__h2">About</h2>
  <table class="section__table">
    <th class="table__th table__th--profile" colspan="2">
      <img class="th__img" v-bind:src="profile" alt="Barbara Zujewska - profile">
    </th>
    <tr class="table__tr" v-for="(value, propertyName, index) in content" v-bind:key="index">
      <th class="tr__th tr__th--label">{{ propertyName }}:</th>
      <th v-if="Array.isArray(value)" class="tr__th tr__th--list">
        <List :content="value" />
      </th>
      <th v-else class="tr__th tr__th--content">{{ value }}</th>
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

.section__h2 {
  width: 70%;
  margin: 0 auto 0;
  /* padding-top: 0.8rem;
  padding-bottom: 9rem; */
}

.section__table {
  width: 70%;
  margin-left: auto;
  margin-right: auto;
  font-size: 1rem;
  grid-column-start: 2;
  grid-column-end: five;
  grid-row-start: row1-start;
  grid-row-end: 3;
}

.tr__th {
  text-align: left;
  vertical-align: top;
  font-weight: normal;
  padding-top: 1rem;
}

.th__img {
  /* position: absolute; */
  height: 15rem;
  border-radius: 50%;
  right: 15%;
  top: 12%;
  position: relative;
  display: block;
  margin: 10px 0 -70px auto;
  text-align: right;
  right: auto;
  top: auto;
}

.tr__th--label {
  font-weight: 800;
}

.tr__th--content {
  margin-left: 3rem;
  padding-bottom: 1rem;
  padding-left: 6rem;
}

.tr__th--list {
  padding-left: 6rem;
}

.table__tr {
  border-bottom: 5px solid #0C5887;
}

.table__tr:last-child {
  border: 0;
}


@media screen and (max-width: 1000px) {
  .section__h2 {
  padding-bottom: 1rem;
  }

  .th__img {
    position: relative;
    display: block;
    margin: 10px auto 10px;
    text-align: center;
    right: auto;
    top: auto;
  }
}

@media screen and (max-width: 800px) {
  
  .section__table {
    width: 90%
  }

  .tr__th--content {
    margin-left: 3rem;
    padding-bottom: 1rem;
    padding-left: 3rem;
  }

  .tr__th--list {
    padding-left: 3rem;
  }
}
</style>
