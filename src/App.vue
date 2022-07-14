<script>
//import HelloWorld from "./components/HelloWorld.vue";
//import TheWelcome from "./components/TheWelcome.vue";
import Header from "./components/Header.vue";
import Blurb from "./components/Blurb.vue";
import BoxyFittedSelector from "./components/BoxyFittedSelector.vue";
import TeeDesigner from "./components/TeeDesigner.vue";
import ContactPage from "./components/ContactPage.vue";

export default {
  components: {
    Header,
    Blurb,
    BoxyFittedSelector,
    TeeDesigner,
    ContactPage,
  },
  data() {
    return {
      pageNumber: 0,
    };
  },
  methods: {
    goToDesignPage() {
      this.pageNumber = 1;
    },
  },
};
</script>

<template>
  <div id="header">
    <Header />
  </div>

  <div id="blurb">
    <Blurb :page-Index="pageNumber" />
  </div>

  <div v-if="pageNumber == 0">
    <BoxyFittedSelector @change-page-index="goToDesignPage()" />
  </div>

  <div v-if="pageNumber == 1">
    <TeeDesigner />
  </div>

  <div v-if="pageNumber == 5">
    <ContactPage />
  </div>
</template>

<style>
@import "./assets/base.css";
@import url("https://fonts.googleapis.com/css2?family=Alata&family=Inknut+Antiqua:wght@900&display=swap");

#app {
  margin: 0 auto;
  font-weight: normal;
  max-width: 100%;
}

#header {
  max-width: 1280px;
  width: auto;
  height: 40px;
  padding: 2rem;
}

#blurb {
  height: 30%;
  padding: 2rem;
}

.row {
  display: flex;
}

.halfcol {
  flex: 50%;
  float: left;
}
</style>
