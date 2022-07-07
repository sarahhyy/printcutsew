<template>
  <div class="row">
    <div class="halfcol" v-on:click="$emit('change-page-index')"><img class="squareImg" src="/src/assets/images/selectBoxysq.jpg">
      <div id="boxy">boxy</div>
    </div>
    <div class="halfcol" @click="$emit('change-page-index')"><img class="squareImg" src="/src/assets/images/selectFittedsq.jpg">
      <div id="fitted">fitted</div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'BoxyFittedSelector',
    props: {
      pageIndex: Number
    },

    emits: ['change-page-index'],

    data () {
      return {
        pageNumber: 0
      }
    },

    methods: {
    goToDesignPage () {
      pageNumber = 1
    }
  }
  }



</script>

<style>
pre {
  text-align: center;
  font-family: 'Alata', Verdana, Geneva, Tahoma, sans-serif;
  color: black;
  font-size: small;
}

div {
  margin:auto;
  width: auto;
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