<template>
  <div class="row designer">
    <div class="arrow-col" @click="changeNeckMinus()">
        <img src="/src/assets/images/icons/arrowleft.png">
    </div>
    <div>
      <img class="layer-design" :src="neckAssets[neckNum]" />
    </div>
    <div class="arrow-col" @click="changeNeckPlus()">
        <img src="/src/assets/images/icons/arrowright.png">
    </div>
  </div>

  <div class="row designer">
    <div class="arrow-col" @click="changeSleeveMinus()">
        <img src="/src/assets/images/icons/arrowleft.png">
    </div>
    <div>
      <img class="layer-design" :src="looseSleeveAssets[looseSleeveNum]" />
    </div>
    <div class="arrow-col" @click="changeSleevePlus">
        <img src="/src/assets/images/icons/arrowright.png">
    </div>
  </div>

  <div class="row designer">
    <div class="arrow-col" @click="changeBodyMinus()">
        <img src="/src/assets/images/icons/arrowleft.png">
    </div>
    <div>
      <img class="layer-design" :src="looseBodyAssets[looseBodyNum]" />
    </div>
    <div class="arrow-col" @click="changeBodyPlus">
        <img src="/src/assets/images/icons/arrowright.png">
    </div>
  </div>
  
</template>

<script>
  export default {
    name: 'TeeDesigner',
    props: {
      neckNum: Number,
      looseSleeveNum: Number,
      looseBodyNum: Number
    },

    data () {
      return {
        neckNum: 0,
        looseSleeveNum: 0,
        looseBodyNum: 0,
        neckAssets: [
          "/src/assets/designChoiceAssets/Neck - Crew.png", 
          "/src/assets/designChoiceAssets/Neck - V.png"
        ],
        looseSleeveAssets: [
          "/src/assets/designChoiceAssets/Loose Sleeve - short straight.png",
          "/src/assets/designChoiceAssets/Loose Sleeve - short slant.png",
          "/src/assets/designChoiceAssets/Loose Sleeve - mid slant.png",
          "/src/assets/designChoiceAssets/Loose Sleeve - long.png"
        ],
        looseBodyAssets: [
          "/src/assets/designChoiceAssets/Loose Body - mid.png",
          "/src/assets/designChoiceAssets/Loose Body - short.png",
          "/src/assets/designChoiceAssets/Loose Body - knee.png"
        ]
      }
    },

    methods: {
      changeNeckPlus () {
      this.neckNum = (this.neckNum + 1) % this.neckAssets.length;
    },
      arrowPlus(arrayIndex, srcArray) {
        arrayIndex = (arrayIndex + 1) % srcArray.length;
    },
      changeNeckMinus () {
        return (this.neckNum == 0 ? this.neckNum = this.neckAssets.length-1 : this.neckNum -= 1)
    },
      changeSleevePlus () {
      this.looseSleeveNum = (this.looseSleeveNum + 1) % this.looseSleeveAssets.length;
    },
      changeSleeveMinus () {
        return (this.looseSleeveNum == 0 ? this.looseSleeveNum = this.looseSleeveAssets.length-1 : this.looseSleeveNum -= 1)
    },
      changeBodyPlus () {
      this.looseBodyNum = (this.looseBodyNum + 1) % this.looseBodyAssets.length;
    },
      changeBodyMinus () {
        return (this.looseBodyNum == 0 ? this.looseBodyNum = this.looseBodyAssets.length-1 : this.looseBodyNum -= 1)
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