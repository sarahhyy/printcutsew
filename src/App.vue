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
  <div id="header">
    <Header />
  </div>

  <div id="blurb">
    <Blurb :page-index="pageNumber"/>
  </div>

  <div class="row">
    <div class="halfcol" v-on:click="goToDesignPage"><img class="squareImg" src="/src/assets/images/selectBoxysq.jpg">
      <div id="boxy">boxy</div>
    </div>
    <div class="halfcol" @click="goToDesignPage"><img class="squareImg" src="/src/assets/images/selectFittedsq.jpg">
      <div id="fitted">fitted</div>
    </div>
  </div>
</template>

<style>
@import "./assets/base.css";
@import url('https://fonts.googleapis.com/css2?family=Alata&family=Inknut+Antiqua:wght@900&display=swap');

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

#boxy {
  position: absolute;
  top: 50%;
  right: 15%;
  font-family: 'Inknut Antiqua', serif;
  font-size: 60px;
  color: white;
}

#fitted {
  position: absolute;
  top: 50%;
  left: 15%;
  font-family: 'Inknut Antiqua', serif;
  font-size: 60px;
  color: white;
}

.row {
  display: flex;
}
.halfcol {
  flex: 50%;
  float: left;
}

.squareImg {
  width: 100%;
  object-fit: contain;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}
</style>
