<template>
  <div class="container">
    <h3>Child 3</h3>
    <div class="content">
      <button class="orange" @click="setOrange">Orange</button>
      <button class="pink" @click="setPink">Pink</button>
      <button class="lightGreen" @click="setLightGreen">Light green</button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    setOrange() {
      this.$emit("setOrangeFromChild3");
    },

    setPink() {
      this.$emit("setPinkFromChild3");
    },

    setLightGreen() {
      this.$emit("setLightGreenFromChild3");
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

  .orange {
    background: orange;
    color: black;
  }

  .pink {
    background: pink;
    color: black;
  }

  .lightGreen {
    background: lightgreen;
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
