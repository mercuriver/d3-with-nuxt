<template>
  <div id="d3_layout">
    <svg></svg>
  </div>
</template>

<script>
import * as d3 from "d3";

const classSelector = (holder, target) => {
  holder.select(`g.${target}`).size()
    ? holder.select(`g.${target}`)
    : holder.append("g").attr("class", target);
};

export default {
  data() {
    handler: null;
  },
  mounted() {
    console.log(d3);
  },
  methods: {
    initScene() {
      const holder = d3.select("#d3_layout svg");

      const links = classSelector(holder, "links");
      const nodes = classSelector(holder, "nodes");
      const descs = classSelector(holder, "descs");
    },
  },
};
</script>

<style scoped>
#d3_layout {
  background-color: aliceblue;
  border: 1px solid salmon;
  width: 100%;
  height: 100%;
}

svg {
  width: 100%;
  height: 100%;
}
</style>
