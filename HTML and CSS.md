#### Character entities
In order to print special characters or tag themselves we use char entities. It starts with &
`&lt; &gt;`
```
&frac14; // 1/4
&nbsp; // space
&deg; // degree
&amp; // &
&apos; // *
&quot; // "
```
#### Box Sizing property:
By default the actual width of the element is the sum of its width+padding+border
when set border-box the width will always have  padding and border included


## Table
```
<table>
	<caption>Heading</caption>
	<tr>
		<th>Hi</th>
		<th>Hello</th>
		<th rowspan=3>Byeee</th>
	</tr>
	<tr>
		<td colspan=2>OK</td>
		<td>OK</td>
	</tr>
	<tr>
		<td>NA</td>
		<td>NA</td>
		<td>NA</td>
	</tr>
</table>
```
`rowspan=` and `colspan=` how many cells ka space will one space take
cell spacing and padding: `cellspacing=` will give space between cells `padding=` will give space between cell and content.


## Flexbox

* Flexbox arranges items into rows and items
* Divided as flex items and flex containers
* Any element that has `display: flex` is called a flex container 
* Elements directly inside flex container are called flex items
* We can directly manipulate objects inside the container via adding properties to the parent elements
* `display: flex; justify-content: center;` aligns the content of the flex container in the center. Equivalent to setting `margin: 0 auto` to the child element itself
* justify-content can take many different values: 
	* flext-start
	* flex-end
	* space-around: gives even space between all the elements
	* space-evenly
* `flex: 1` This is shorthand for 3 different declarations `flex-grow`, `flex-basis`, `flex-shrink`
* When flex is set to 1, grow and shrink are set to 1 and basis is set to 0.
* Flex Grow, sets the growth factor for the flex item.
* *when you have the width of the flex items more than the container, the flex items will shrink to fit*
* Flex Shrink sets the shrink factor for the element, in case we want different elements to shrink differently.
* Flex Basis sets the initial size of the element, any growing or shrinking starts from here only. Its basically like, please take up this much space if possible. Otherwise proportional to that.

### Flex Axes
`flex-direction: column;`
There are two directions of flow for flex items, by default it is horizontal or row. We can change the direction using flex-direction property inside the flex-container. 

