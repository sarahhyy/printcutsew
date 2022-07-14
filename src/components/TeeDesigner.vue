<template>
  <div class="row designer">
    <img class="base-design" src="/src/assets/designChoiceassets/Loose Body Base.png" />
  </div>

  <div class="row designer body">
    <div class="body-arrow-col" @click="changeBodyMinus()">
      <img src="/src/assets/images/icons/arrowleft.png" />
    </div>
    <div class="body-image">
      <img class="layer-design" :src="looseBodyAssets[looseBodyNum]" />
    </div>
    <div class="body-arrow-col" @click="changeBodyPlus">
      <img src="/src/assets/images/icons/arrowright.png" />
    </div>
  </div>

  <div class="row designer">
    <div class="arrow-col" @click="changeNeckMinus()">
      <img src="/src/assets/images/icons/arrowleft.png" />
    </div>
    <div>
      <img class="layer-design" :src="neckAssets[neckNum]" />
    </div>
    <div class="arrow-col" @click="changeNeckPlus()">
      <img src="/src/assets/images/icons/arrowright.png" />
    </div>
  </div>

  <div class="row designer">
    <div class="sleeve-arrow-col" @click="changeSleeveMinus()">
      <img src="/src/assets/images/icons/arrowleft.png" />
    </div>
    <div>
      <img class="layer-design sleeve" :src="looseSleeveAssets[looseSleeveNum]" />
    </div>
    <div class="sleeve-arrow-col" @click="changeSleevePlus">
      <img src="/src/assets/images/icons/arrowright.png" />
    </div>
  </div>

</template>

<script>
export default {
  name: "TeeDesigner",
  data() {
    return {
      neckNum: 0,
      looseSleeveNum: 0,
      looseBodyNum: 0,
      neckAssets: [
        "/src/assets/designChoiceAssets/Neck - Crew.png",
        "/src/assets/designChoiceAssets/Neck - V.png",
      ],
      looseSleeveAssets: [
        "/src/assets/designChoiceAssets/Loose Sleeve - short straight.png",
        "/src/assets/designChoiceAssets/Loose Sleeve - short slant.png",
        "/src/assets/designChoiceAssets/Loose Sleeve - mid slant.png",
        "/src/assets/designChoiceAssets/Loose Sleeve - long.png",
      ],
      looseBodyAssets: [
        "/src/assets/designChoiceAssets/Loose Body - mid.png",
        "/src/assets/designChoiceAssets/Loose Body - short.png",
        "/src/assets/designChoiceAssets/Loose Body - knee.png",
      ],
    };
  },

  methods: {
    changeNeckPlus() {
      this.neckNum = (this.neckNum + 1) % this.neckAssets.length;
    },
    arrowPlus(arrayIndex, srcArray) {
      arrayIndex = (arrayIndex + 1) % srcArray.length;
    },
    changeNeckMinus() {
      return (this.neckNum == 0 ? this.neckNum = this.neckAssets.length - 1 : this.neckNum -= 1);
    },
    changeSleevePlus() {
      this.looseSleeveNum = (this.looseSleeveNum + 1) % this.looseSleeveAssets.length;
    },
    changeSleeveMinus() {
      return (this.looseSleeveNum == 0 ? this.looseSleeveNum = this.looseSleeveAssets.length - 1 : this.looseSleeveNum -= 1);
    },
    changeBodyPlus() {
      this.looseBodyNum = (this.looseBodyNum + 1) % this.looseBodyAssets.length;
    },
    changeBodyMinus() {
      return (this.looseBodyNum == 0 ? this.looseBodyNum = this.looseBodyAssets.length - 1 : this.looseBodyNum -= 1);
    },
  },
};
</script>

<style>
pre {
  text-align: center;
  font-family: "Alata", Verdana, Geneva, Tahoma, sans-serif;
  color: black;
  font-size: small;
}

div {
  margin: auto;
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
  position: absolute;
  top: 8px;
  z-index: 0;
  left: 41.8%;
  right: 42%;
}

.layer-design {
  z-index: 10;
  align-self: top;
}

.neckline {
  height: 110px;
}

.sleeve {
  height: 350;
  margin-top: -26px;
}

.sleeve-arrow-col {
  margin-top: 40px;
  margin-left: 0;
  margin-right: 0;
  width: 40px;
}

.body-arrow-col {
  margin-top: 40px;
  margin-left: 0;
  margin-right: 0;
  width: 40px;
}

.body {
  position: absolute;
  top: 160px;
  left: 21.85%;
}

.body-image {
  margin: 0;
}
</style>
