<template>
  <div id="app">
    <div>
      <hscroll-table :rows="rows" :cols="cols" />
    </div>
  </div>
</template>

<script>
import HscrollTable from "./components/HscrollTable.vue";

export default {
  name: "App",
  components: {
    HscrollTable,
  },
  data() {
    return {
      cols: [],
      rows: [],
    };
  },
  mounted() {
    for (let col = 0; col < 30; col++) this.cols.push({ key: "text" + col });

    for (let row = 1; row < 200; row++) {
      let item = {
        class:
          row % 10 == 0
            ? "scrollrow"
            : row % 10 == 1
            ? "hilight1"
            : row % 10 == 9
            ? "hilight2"
            : "",
      };
      for (let col = 0; col < 30; col++)
        item["text" + col] = "Row " + row + " Col " + col;

      this.rows.push(item);
    }
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
