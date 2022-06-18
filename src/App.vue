<script setup lang="ts">
//import HelloWorld from "./components/HelloWorld.vue";
//import TheWelcome from "./components/TheWelcome.vue";
import Header from "./components/Header.vue";
import Blurb from "./components/Blurb.vue";
undefined
</script>

<template>
  <div>
    <Header />
  </div>

  <div>
    <Blurb />
  </div>
  <main>
    <div>//add one component here.</div>
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
