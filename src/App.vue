<script>
//import HelloWorld from "./components/HelloWorld.vue";
//import TheWelcome from "./components/TheWelcome.vue";
import Header from "./components/Header.vue";
import Blurb from "./components/Blurb.vue";

export default {
  components: {
    Header,
    Blurb
  },
  data () {
    return {
      pageNumber: 0
    }
  },
  methods: {
    goToDesignPage () {
      this.pageNumber = 1
    }
  }
}
</script>

<template>
  <div>
    <Header />
  </div>

  <div>
    <Blurb :page-index="pageNumber"/>
  </div>
  <main>
    <div v-on:click="goToDesignPage">//add one component here.</div>
    <div>//add same component but different content here (does it work that way?)</div>
  </main>
</template>

<style>
@import "./assets/base.css";
@import url('https://fonts.googleapis.com/css2?family=Alata&family=Inknut+Antiqua:wght@900&display=swap');

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;
  font-weight: normal;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}
</style>
