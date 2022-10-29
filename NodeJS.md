## NodeJS
Instead of browser specific APIs, NodeJS provides APIs for more of general OS use, such as HTTP.
Process is an object that gives us access to control the running NodeJS process

Node creates the server.... and that's it, for more specific handling of requests requires either us to write the code, or using something like Express.

*VV Important that we use Non Blocking Asynchronous functions for Node as it is a Single Threaded Execution Environment* 

Every I/O must take a callback
Built-in support for HTTPS, DNS and TLS
Never force the buffering of data

Using a large amount of callbacks willynilly can lead you to callback hell, this is why most of the complex operations are taken care by using functions:
* Initiator/input: First function in the sequence, has acess to global vars.
* Middleware: Returns another function
* Terminator: Involves callback
```
function final(someInput, callback){
	callback(someInput)
}

function middleware(someInput, callback){
	console.log('inside middleware');
	final(someInput, callback);
}

function init(){
	console.log("inside init");
	middleware('resssssult', (res)=>{
		console.log(res);
	})
}

init();
```

*Suppose we fetch some info from the network, it takes some time to be fetched which is known as latency. Let the data be stored in a var called result and we return that var at the end of the same function. There is huge amount of chance that a null value will be returned by the function because the fetch instrutction like the setTimeout instruction is async.*
In order to avoid the above scenario without blocking the control of entire browser, we use callbacks.

### Functions
* `const http = require(http)` require() is an inbuilt function used to load up modules that might be present in another external directory, reads the JS files, executes it and returns the exported object
* `http.createServer(function)` creates an HTTP server 
* `server.listen(port, host, function)`: Function is called when the server is ready
* Whenever a request is made to the server a request event is called with two objects request (http.IncomingMessage) and response (http.ServerResponse)


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