## Basic Syntax

When creating a new single page application its best to create a new React app. Otherwise the easiest method is to include a couple of script tags
```
import React from "react"
import ReactDOM from "react-dom/client"
import "./index.css"
```

Now you can continue with using JSX code, as you want.

In react we make different components to work with in an object oriented fashion.
A typical component declaration looks like,
```
class HelloWorld extends React.Component {
	render(){
		return (
			<div>
				<h1> 
					HAIIILLLOOOOO
				</h1>
			</div>
		)
	}	
}
```

Now this entire component can be used directly using `<HelloWorld/>`

React Components have something called props class which stores all the parameters that is passed to the element when calling it
e.g.
`<square value=1/>`
Now you can access the value
`this.props.value`  inside the square class.

* In order to remember something and work with values, we use *states*, In React, a state is defined inside the components constructor function that needs to be declared explicitly.
* Since all the React components are subclasses the function super(props) needs to be used inside the constructor class.

Code is something like this
```
class Square extends React.component{
	constructor(props){
		super(props);
		this.state = {
			value: NULL,
		};
	}
	
	render(){
		return (
			//code here
		)
	}
}
```

* In JS for making an array you need to use the function `Array(size)` 
* *Array().slice() creates a copy of the array in order to preserve the original array*
```
constructor(props){
		super(props);
		this.state = {
			value: Array(9).fill(null),
		};
	}
```

* If you are looking for interaction between two different components, you need to use props
e.g
```
class Square extends React.Component {  render() {    return (
      <button
        className="square"
        onClick={() => this.props.onClick()}>
        {this.props.value}      </button>
    );
  }
}

class Board extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      squares: Array(9).fill(null),
    };
  }

  handleClick(i) {    const squares = this.state.squares.slice();    squares[i] = 'X';    this.setState({squares: squares});  }
  renderSquare(i) {
    return (
      <Square
        value={this.state.squares[i]}
        onClick={() => this.handleClick(i)}
      />
    );
  }
```
Here the onClick property of the Square component is changed by the Board method and therefore in order to access it inside the Sqaure Class itself we need to use `this.props.onClick`

* If a component only has a render element and no constructors and other methods, we build these components using functions instead of classes
* e.g. the square component in the above example:
```
function Sqaure(props){
	return (
		<button className="square" onClick={props.onClick}>
		{props.value}
		</button>
	);
}
```
*Notice the lack of paranthesis

