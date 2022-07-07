<template>
  <div class="row designer">
    <div class="arrow-col">
        <img src="/src/assets/images/icons/arrowleft.png">
    </div>
    <div>
      <img src={{neckAssets}}>
    </div>
    <div class="arrow-col" @click="changeNeck()">
        <img src="/src/assets/images/icons/arrowright.png">
    </div>
  </div>
  
</template>

<script>
  export default {
    name: 'TeeDesigner',
    props: {
      neckAssets: Number
    },

    data () {
      return {
        neckAssets: [
          "/src/assets/designChoiceAssets/Neck - Crew.png", 
          "/src/assets/designChoiceAssets/Neck - V.png"
        ]
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

.designer {
  margin: auto;
  width: 1080px;
  min-width: 1080px;
  border: 5px black;
  justify-content: space-between;
}

.arrow-col {
  margin: 0;
  width: 40px;
}

.neckline {
  height: 110px;
}

.sleeve {
  height: 350;
}

.body-length {
  height: 300;
}

</style>