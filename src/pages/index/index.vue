<template>
  <virtual-list
    wclass="List"
    :height="500"
    :item-data="list"
    :item-count="list.length"
    :item-size="100"
    :item="Row"
    width="100%"
  />
</template>

<script>
import Row from "./row.vue";

function buildData(offset = 0) {
  return Array(100)
    .fill(0)
    .map((_, i) => i + offset);
}
export default {
  name: "Index",
  data() {
    return {
      Row,
      list: buildData(0)
    };
  }
};
</script>

<style>
.index {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
