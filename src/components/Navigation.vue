<template>
<nav class="nav">
  <div class="nav__div--wrapper">

    <h1 class="wrapper__h1 wrapper__h1--widescreen">
      <ScrollLink :id="widescreen" />
    </h1>
    <h1 class="wrapper__h1 wrapper__h1--mobile">
      <ScrollLink :id="mobile" />
    </h1>

    <div class="wrapper__div--menu">
      
      <ul class="menu__ul" >
        <li class="ul__li" v-for="(id, index) in sections" v-bind:key="index">
          <ScrollLink :id="id" />
        </li>
      </ul>

      <div class="menu__wrapper--hamburger" @click="openMenu()">
        <button class="hamburger hamburger--collapse hamburger--accessible js-hamburger" type="button">
          <span class="hamburger-label">Menu</span>
          <span class="hamburger-box">
            <span class="hamburger-inner"></span>
          </span>
        </button>
      </div>

    </div>

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
      mobile: 'BZuj',
      widescreen: 'Barbara Zujewska',
      sections: ['About', 'Tools', 'Projects', 'Contact']
    }
  },
  methods: {
    openMenu() {
      const menu = document.querySelector(`.menu__ul`);
      menu.classList.toggle('menu__ul--mobileopen');
      const hamburger = document.querySelector(`.js-hamburger`);
      hamburger.classList.toggle('is-active');
    }
  }
}

</script>

<style>
@import './styles/hamburger.css';

.nav {
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

.wrapper__h1 {
  cursor: pointer;
}

.wrapper__h1--widescreen {
  display: block;
}

.wrapper__h1--mobile {
  display: none;
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

.menu__img {
  display: none;
}

.menu__ul {
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

@media only screen and (max-width: 768px) {
  .wrapper__h1--widescreen{
    display: none;
  }

  .wrapper__h1--mobile{
    display: block;
  }

  .menu__ul {
    display: none;
    /* z-index: -1; */
  }
  

  .menu__ul--mobileopen {
    display: block;
    position: fixed;
    -webkit-flex-flow: column nowrap;
    -moz-box-orient: vertical;
    -moz-box-direction: normal;
    flex-flow: column nowrap;
    /* backdrop-filter: blur(40px); */
    background-color: #001e30cc;
    top: 0;
    right: 0;
    height: 100vh;
    width: 170px;
    margin: 0;
    padding: 50px 30px;
  }

  .ul__li {
    padding: 30px 0 0;
    border-right: none;
    color: white;
    font-weight: 500;
    font-size: 1.3rem;
  }

}

</style>