<template>
  <div class="parent-container">
    <h2>Parent</h2>
    <div class="workText" :class="color">Test text</div>
    <div class="parent-content">
      <first-child
        @setRedFromChild1="setRed"
        @setGreenFromChild1="setGreen"
        @setBlueFromChild1="setBlue"
      />
      <second-child
        @setVioletFromChild2="setViolet"
        @setGoldFromChild2="setGold"
        @setSilverFromChild2="setSilver"
      />
      <third-child
        @setOrangeFromChild3="setOrange"
        @setPinkFromChild3="setPink"
        @setLightGreenFromChild3="setLightGreen"
      />
    </div>
  </div>
</template>

<script>
import FirstChild from "./Child-1.vue";
import SecondChild from "./Child-2.vue";
import ThirdChild from "./Child-3.vue";
export default {
  data() {
    return {
      color: "",
    };
  },
  methods: {
    setRed() {
      this.color = "colorRed";
    },
    setGreen() {
      this.color = "colorGreen";
    },
    setBlue() {
      this.color = "colorBlue";
    },
    setViolet() {
      this.color = "colorViolet";
    },
    setGold() {
      this.color = "colorGold";
    },
    setSilver() {
      this.color = "colorSilver";
    },
    setOrange() {
      this.color = "colorOrange";
    },
    setPink() {
      this.color = "colorPink";
    },
    setLightGreen() {
      this.color = "colorLightGreen";
    },
  },

  components: { FirstChild, SecondChild, ThirdChild },
};
</script>

<style lang="scss">
.parent-container {
  padding: 30px;
  border: 1px solid rgb(255, 0, 0);

  h2 {
    text-align: center;
  }

  .workText {
    width: 30%;
    margin: 0px auto 30px;
    padding: 10px;
    text-align: center;
    font-size: 30px;
    border: 1px solid white;
  }

  .colorRed {
    color: red;
  }

  .colorGreen {
    color: green;
  }

  .colorBlue {
    color: blue;
  }

  .colorViolet {
    color: darkviolet;
  }

  .colorGold {
    color: gold;
  }

  .colorSilver {
    color: silver;
  }

  .colorOrange {
    color: orange;
  }

  .colorPink {
    color: pink;
  }

  .colorLightGreen {
    color: lightgreen;
  }
}

@media (max-width: 1200px) {
  .parent-content {
    display: flex;
    flex-direction: column;
  }
}

.parent-content {
  display: flex;
  justify-content: space-evenly;
}
</style>
