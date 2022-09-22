## Jquery
Contains a set of JS code to make my life easier (Thanks Jquery)

Import and all shit u do

```
$(document).ready(function (){
	$("p").click(function (){
		$(this).hide()
	})
})
```

document is basically DOM, click is onClick, this is event.target
Between two different jQuery elements there needs to be a comma

`$(selector).action()`

*JS objects are by default available to the scripts*
`$(document).ready(func(){})`

The ready function prevents any jQuery code from running before the page is loaded.

### Manipulate Elements
`.click()` adds click event listener
`.hide()` hides the element
`.show()` shows the element
`.toggle()` toggles the state

### DOM Manipulation
`.before()` Before the ele
`.after()` After the ele
`.append()` Appends to the ele
`.appendTo()` Appends the ele

### Attribute Functions
`.css()` changes the css
`.addClass()` adds class attrib to the ele
`.attr()` returns the value for the passed attribute or replaces the attrib

All these methods work as both getters and setters

### Events 
`.click()` Adds event click
`.bind()` 
`.unbind()`
`.live()`

### Callback
Callback functions get added into a queue and executed accordingly. First all the functions before callback get executed


### Promises
Pomises are used when making request to an external site for a heavy resource or a long calculation to do work, REST APIs etc. When the latter becomes availableor the request has failed.

### Deferred
These objects are implementations of Promises in jQuery
`always()`, `done()`, `fail()`, `state()`, `then()`
