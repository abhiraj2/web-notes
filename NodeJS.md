## NodeJS
Instead of browser specific APIs, NodeJS provides APIs for more of general OS use, such as HTTP.

Node creates the server.... and that's it, for more specific handling of requests requires either us to write the code, or using something like Express.

*VV Important that we use Non Blocking Asynchronous functions for Node as it is a Single Threaded Execution Environment* 

### Functions
* `const http = require(http)` require() is an inbuilt function used to load up modules that might be present in another external directory, reads the JS files, executes it and returns the exported object
* `http.createServer(function)` creates an HTTP server 



## ExpressJS
Express is just a node module 

```
const express = require("express")
const app = express()
```

This creates a basic Express application

```
app.get('/', function(req, res){
	res.send("Hello World");
})
```
This creates a route for the app where it specifies that whenever a get request is sent to `'/'` URL, you call the following function


Even Express by itself is quite minimalistic, therefore we use Middlewares in order to increase its functionality