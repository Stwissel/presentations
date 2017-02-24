##  Demo results

In a short moment we did:

* create a new Hoodie:<br /> ```var hoodie = new Hoodie();```
* register a user:<br /> ```hoodie.account.signUp('username','password');```
* store data:<br /> ```hoodie.store.add('food', {id:'Durian', color:'white', smell:'century socks' });```
* retrieve data:<br /> ```hoodie.store.findAll('food').done(function(foods) {/* action here */} );```

note:
   Highlight how easy it was to build the application
