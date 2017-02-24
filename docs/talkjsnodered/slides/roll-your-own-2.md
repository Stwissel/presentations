##  mynode.js

		module.exports = function(RED) {
		    "use strict";
		
		    function MyNode(n) {
		        // Create a RED node
		        RED.nodes.createNode(this,n);
		        var node = this;
		        node.name = n.name;
		        node.field = n.field || "payload";
		        
		        // Clean the payload object
		        this.on('input', function (msg) {
					var raw = msg[node.field] || {};			
					try {
						// here is the work!
						msg[node.field] = {"answer" : "42 what else?"};
						
						// Done
						this.status({fill:"green",shape:"dot",text: "We rock"});
						node.send([msg]);		
		            } catch(err) {
						this.status({fill:"red",shape:"dot",text: err.message});
		                node.error(err.message);
		            }
		            
		        });
		
		        this.on("close", function() {
		            // No action so far
		        });
		    }
		    RED.nodes.registerType("mynode",MyNode);		
		}
	
