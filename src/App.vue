<template>
  <div>
    <h1>Root component</h1>
    <div class="content">
      <parent-comp />
    </div>
  </div>
</template>

<script>
import ParentComp from "./components/Parent-Comp.vue";
export default {
  components: { ParentComp },
};
</script>

<style lang="scss">
:root {
  width: 70%;
  margin: 0 auto;
  padding: 0;
  color: white;
  font-family: sans-serif;
  background: #222;
  border: 1px solid blue;

  h1 {
    text-align: center;
  }
}
</style>
