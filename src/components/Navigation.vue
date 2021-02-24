<template>
<nav class="nav">
  <div class="nav__div--wrapper">
    <h1>Barbara Zujewska</h1>
      <ul class="wrapper__ul" >
        <li class="ul__li" v-for="(id, index) in sections" v-bind:key="index">
          <ScrollLink :id="id" />
        </li>
    </ul>
  </div>
</nav>
</template>

<script>
import ScrollLink from './ScrollLink.vue';
export default {
  name: "Navigation",
  components: {
    ScrollLink,
  },
  data() {
    return {
      sections: ['About', 'Tools', 'Projects', 'Contact']
    }
  }
}

</script>

<style>
.nav {
  /* background: rgb(255,255,255);
  background: linear-gradient(180deg, rgba(255,255,255,1) 0%, rgba(255,255,255,1) 20%, rgba(212,236,250,1) 100%); */
  display: flex;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  width: 100%;
  height: 50px;
  z-index: 1;

  backdrop-filter: blur(10px);
  

  -webkit-box-pack: center;
  -webkit-box-align: center;
}
.nav__div--wrapper {
  width: 80%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  max-width: 1100px;
  font-size: 1rem;
  margin: 0 auto
}


.wrapper__ul {
  list-style: none;
  display: flex;
  align-items: center;
  text-align: center;

  -webkit-box-align: center;
}

.ul__li {
  padding: 0 10px;
  border-right: thin solid #083D5E;
  cursor: pointer;
}

.nav li:last-of-type {
  border-right-style: none;
}

</style>