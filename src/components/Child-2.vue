<template>
  <div class="container">
    <h3>Child 2</h3>
    <div class="content">
      <button class="violet" @click="setViolet">Violet</button>
      <button class="gold" @click="setGold">Gold</button>
      <button class="silver" @click="setSilver">Silver</button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    setViolet() {
      this.$emit("setVioletFromChild2");
    },
    setGold() {
      this.$emit("setGoldFromChild2");
    },
    setSilver() {
      this.$emit("setSilverFromChild2");
    },
  },
};
</script>

<style lang="scss" scoped>
.container {
  padding: 10px;
  border: 1px solid green;

  h3 {
    text-align: center;
  }

  button {
    margin: 2px;
  }

  .violet {
    background: darkviolet;
    color: black;
  }

  .gold {
    background: gold;
    color: black;
  }

  .silver {
    background: silver;
    color: black;
  }
}

@media (max-width: 1200px) {
  .content {
    display: flex;
    justify-content: space-between;
    padding: 10px;
  }

  button {
    width: 30%;
    margin: 0 auto;
  }
}
</style>
