<template>
  <div id="app" class="app">
    <Header v-bind:list="list" />
    <Hero />
    <Nav />
    <Socials v-bind:socials="list.social_media" />
  </div>
</template>

<script>
import Vue from 'vue'
import axios from 'axios'
import vueAxios from 'vue-axios'

// component imports
import Header from './components/Header.vue';
import Hero from './components/Hero.vue'
import Nav from './components/Nav.vue'
import Socials from './components/Socials.vue'

Vue.use(vueAxios, axios)

export default {
  name: 'App',
  components: {
    Header,
    Hero,
    Nav,
    Socials
  },
  data() {
    return {
      list: []
    }
  },
  mounted() {
      Vue.axios.get('https://hirng-x2021.glitch.me/api')
      .then((res) => {
        console.warn(res.data);
        this.list = res.data;
      })
  }
}
</script>

<style lang="scss">
/* globals */
@import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400&display=swap');

:root {
  /* colors */

  --primary_clr: #BD0F4D;
  --secondary_clr: #CB2964;
  --white: #fcfcfc;

  --spacer: 1rem;
}

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

html {
  font-size: 62.5%;
}

body {
  font-family: 'Quicksand', sans-serif;
  color: var(--white);
  font-size: 1.6rem;
  overflow: hidden;
  background: linear-gradient(90deg, var(--primary_clr) 50%, var(--secondary_clr) 50%);
  background-repeat: no-repeat;
}

a {
  text-decoration: none;
  color: var(--white);
}

.app {
  min-height: 100vh;
  width: 100%;
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  overflow: hidden;
}

</style>
