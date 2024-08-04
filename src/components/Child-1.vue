<template>
  <div class="container">
    <h3>Child 1</h3>
    <div class="content">
      <button class="red" @click="setRed">Red</button>
      <button class="green" @click="setGreen">Green</button>
      <button class="blue" @click="setBlue">Blue</button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    setRed() {
      this.$emit("setRedFromChild1");
    },

    setGreen() {
      this.$emit("setGreenFromChild1");
    },
    setBlue() {
      this.$emit("setBlueFromChild1");
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

  .red {
    background: red;
    color: black;
  }

  .green {
    background: green;
    color: black;
  }

  .blue {
    background: blue;
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
