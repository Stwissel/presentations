##  mynode.js
<br />

	  function MyNode(n) {
      RED.nodes.createNode(this,n);
      this.on('input', function (msg) {
      this.on("close", function() {
      RED.nodes.registerType("mynode",MyNode);

