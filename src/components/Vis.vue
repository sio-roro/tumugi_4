<template>
  <div class="main">
    {{ message }}
    <div id="mynetwork"></div>
  </div>
</template>
<script
  type="text/javascript"
  src="https://unpkg.com/vis-network/standalone/umd/vis-network.min.js"
></script>
<script>
var nodes = {};
var edges = {};
var container = {};
var data = {};
var options = {};
var network = {};

export default {
  name: "app",
  mounted: function() {
    // create an array with nodes
    nodes = new vis.DataSet([
      { id: 1, label: "sio", group: "", chosen: true, color: "#8cd790" },
      { id: 2, label: "yuya", group: "", chosen: true, color: "#8cd790" },
      { id: 3, label: "reo", group: "", chosen: true, color: "#8cd790" },
      { id: 4, label: "sumi", group: "", chosen: true, color: "#8cd790" },
      { id: 5, label: "sen", group: "", chosen: true, color: "#8cd790" },
    ]);

    // create an array with edges

    edges = new vis.DataSet([
      { from: 3, to: 4, arrows: "to", width: 2, color: { color: "red" } },
      { from: 1, to: 2 },
      { from: 2, to: 4 },
    ]);

    // create a network
    container = document.getElementById("mynetwork");

    // provide the data in the vis format:
    data = {
      nodes: nodes,
      edges: edges,
    };

    options = {};

    // initialize your network!
    network = new vis.Network(container, data, options);
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.main {
  color: red;
}
</style>
