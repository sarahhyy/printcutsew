<template>
  <div class="row designer">
    <div class="arrow-col" @click="changeNeckMinus()">
        <img src="/src/assets/images/icons/arrowleft.png">
    </div>
    <div>
      <!--<img class="base-design" src="/src/assets/designChoiceAssets/Loose Body Base.png">-->
      <img class="layer-design" :src="neckAssets[neckNumber]" />
    </div>
    <div class="arrow-col" @click="changeNeckPlus()">
        <img src="/src/assets/images/icons/arrowright.png">
    </div>
  </div>
  
</template>

<script>
  export default {
    name: 'TeeDesigner',
    props: {
      neckNumber: Number
    },

    data () {
      return {
        neckNumber: 0,
        neckAssets: [
          "/src/assets/designChoiceAssets/Neck - Crew.png", 
          "/src/assets/designChoiceAssets/Neck - V.png"
        ]
      }
    },

    methods: {
      changeNeckPlus () {
      this.neckNumber = (this.neckNumber + 1) % this.neckAssets.length;
    },
      changeNeckMinus () {
        if (this.neckNumber == 0) {
          this.neckNumber = this.neckAssets.length -1;
        } else {
          this.neckNumber -= 1;
        }
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

.base-design {
  z-index: 0;
}

.layer-design {
  z-index: 10;
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