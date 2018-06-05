<h2>mynode.html</h2>
<pre>
&lt;script type="text/x-red" data-template-name="mynode"&gt;
    &lt;div class="form-row"&gt;
        &lt;label for="node-input-name"&gt;&lt;i class="fa fa-tag"&gt;&lt;/i&gt; Name&lt;/label&gt;
        &lt;input type="text" id="node-input-name" placeholder="Name"&gt;
    &lt;/div&gt;

    &lt;div class="form-row"&gt;
        &lt;label for="node-input-field"&gt;&lt;i class="fa fa-tag"&gt;&lt;/i&gt; Property&lt;/label&gt;
        &lt;input type="text" id="node-input-field" placeholder="payload"&gt;
    &lt;/div&gt;
&lt;/script&gt;

&lt;script type="text/x-red" data-help-name="mynode"&gt;
	
   &lt;p&gt;Gives you the final answer!&lt;/p&gt;
  
&lt;/script&gt;

&lt;script type="text/javascript"&gt;
    RED.nodes.registerType('mynode',{
        category: 'experimental', 
        defaults: {
            name: {value:""},
            field: {value:""},           
        },
        inputs:1,
        outputs:1,
        icon: "mynode.png",
        color : "#ffdddf",
        label: function() {     // sets the default label contents
            return this.name||"objectcleaner";
        }
    });
&lt;/script&gt;
</pre>
