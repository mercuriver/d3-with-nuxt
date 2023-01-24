<template>
  <h1>Hello world!</h1>
  <div id="d3_layout"></div>
</template>

<script>
import * as d3 from "d3";

export default {
  created() {
    console.log(d3);
  },
};
</script>

<style scoped>
#d3_layout {
  background-color: aliceblue;
  border: 1px solid salmon;
}
</style>
