### Types of vars
<hr>
* without any keyword the variable is  global. Even if decalred inside the function, it will be globally accessible after calling.
* with let: It is restricted to the current block, no hoisting, no redeclaration,child block has access
* with var: rectricted to the current function, hoisting is also done, lets you redeclare the variable, child block has access
* with const: constant, no hoisting, no redeclaration

*Hoisting is the process in which the declaration of the variable gets pushed to the top automatically*

*Operator precedence is left to right*
```
a=10
b="100"
3+a+b // 13100
3-a+b // -7100
```

#### Special functions
* `parseInt(string, num)` : Parses the number out of the string only if it is in the beginning of the string in the base of num. By default it returns decimal value. If the digits are not available in the mentioned base, only till the available digit is parsed rest all are said to fuck off.
* `parseFloat(string)` : ------------do---------------
* `prompt()` lets u get input from the user
* `Number(prompt())` converts string input to number
* `isNAN()` checks if the variable is NaN
* `setInterval(fun, time(ms))` repeats the process every time periodically
* `setTimeout(fun, time(ms))` calls the functions after time milliseconds
* `clearinterval(t)` clears the setInterval command that is stored inside t
* `alert(str)` only one argument allowed
* Document object has a property that is URL and saves the URL for the page as a string. `document.url`

* `Number.toFixed(int)` truncates decimals to 2nd floating point

### Loops
* `a=[4,2,6,9]; for(i in a);` This works as for i in range(len(a))
* `for(i of a);` i becomes the element of a instead of the index


### Functions
*If you pass less number of arguments, the non-matched args get undefined value*
A function may or may not have a name
They can also be event handlers.

### Array
*Partial initialization is always undefined for the rest of the values*
*All the elements in an array are stored internally as a string*
* `push()` appends
* `unshift` prepends
* `pop()` deletes the last element and returns the value
* `shift()` deletes the first element and returns the value
* `join()` returns a string with arr elements
* `slice()` creates a copy of the original array so that it remains unchanged. You can give start and end index also as parameters
* `splice(start, number of elements to delete, arr)` It will change the og array from start to the number of terms with arr
* `sort()` sorts the array in lexicographical order. You can pass another function inside the sort function and it'll work like key in python
*The key implementation is not like Python. It does not work on boolean values. It works on Positive or negative values. If result is negative then swap. Otw keep it as is*

### Strings
Functions
* `myString.replace(old, new)` replaces old phrase with new and returns a new string. old can either be string or regex. When string only the first occurrence is changed.


### Built-in Objects
* Date library `d = new Date()`
	* Now we can use functions from the Date object to fetch date time

### Events
Every event has a block of code that runs when the event occurs and is called event handler
Whenever an event occurs, all the info is 
* onload - It's an event that gets called only when the web page loads `<body onload="init()">`
* `event.key` to access the keys being pressed
* `element.addEventListener(event, handler)`
* `event.clientX` and `event.clientY` will give the X and Y coordinates
* Difference between `event.target` and `event.currentTarget`: The prior one refers to the deepest nested node inside the tag on which the event occurred. So if form contains the onclick event and anywhere inside form is clicked. target refers to the element inside form which was clicked but currentTarget or this will point to form itself.
* `event.type` returns the type of event being triggered
* `event.preventDefault()` prevents the default behaviour of the browser
* `event.stopPropagation()` stops the flow of event at that point

### Event Bubbling and Event Capturing
An event is triggered at the most specific level and then continues upwards, this is called **Event Bubbling**
Opposite of this is called **Event Capturing**

In DOM 2 Event Flow, first Capturing, then Bubbling

### Canvas
HTML element that provides u with a drawing board of your own
```
<canvas class="can">
</canvas>
```
Creates a rectangular canvas
```
const canvas = document.getElementByClass("can")
const ctx = canvas.getContext("2d")
```
The canvas object contains info and properties of the canvas whereas all the drawing are done inside the ctx also called the context of the canvas

##### Canvas Functions
* `ctx.beginPath()` Canvas is sorta like PC logo, so wherever u use this the new inking will start here
* `ctx.clearRect(pos.x, pos.y, canvas.width, canvas.height)` Clears area around x,y of dimensions width and height
* `ctx.arc(center.x, center.y, radius, startAngle, endAngle, CC?)`
* `ctx.fillStyle` property of context that tells the color to fill into the drawn shape
* `ctx.fill()` Fills the drawn shape


### Web Workers


### DOM functions:
DOM is a tree DS therefore is contains Nodes that contain other links to other Nodes
```
<html>
	<head>
		<title>Bruh</title>
	</head>
	<body>
		<h1>Bruhgff</h1>
		<p>Broseph</p>
	</body>
</html>
```
Here the DOM tree starts with html at its root and then head and body as sibling childs of html and so on

* `dom.appendChild(element)` Appends element to the DOM element
* `dom.insertBefore(element1, element2)` Inserts element1 just before element2
* `dom.remove()` Removes the node element from its current parent
* `dom.replaceChild(element1, element2)` element2 gets replaced with element1
* `dom.createTextNode(value)` creates a text node with value as the text, TextNode means just plain normal text inside parent
* `dom.createElement(tag)` creates an empty node of tag type
* `ele.onclick `DOM level 0 event handler
* `addEventListener`
* `removeEventListener`
* `let event = new CustomEvent(name, details)` creates a new event, in order to dispatch it (as in trigger it) you do `ele.dispatchEvent(event)`


#### Mouse Buttons
Event objects passed to the mouse event handler has a property called button that indicates the button pressed
* 0 -> Main button
* 1 -> Middle
* 2 -> Right

#### Event Delegation
It is the process of having only one event handler that handles all events of a particular type.


### JSON
* `JSON.parse(string)`
* `JSON.stringify(obj)`

