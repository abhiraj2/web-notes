## Bootstrap

### Container and Fixed Container
* `container` and `container-fluid`: container sets the width to a fixed amount whereas container-fluid takes up entire width of viewport
* The max-width for Container changes on different screen sizes, for a very small sreen it is 100%
* By default top and bottom padding of a container is 0, therefore we can use sizing utilities to change the padding, e.g. class pt-3 which adds 16px padding to the top
* Stylings such as borders and bg are also applied with classes `border`, `bg-dark` etc.

### Grid System
Built with Flexbox
It is built on 12 columns design, where the max number of colu,n in one row can be 12

To use the grid system make the parent div class to row and the child to `.col-*-*` the first star is replaced with size and the second star is replaced with the span number. Span number across all the children must be 12

* `.col-`: Extra Small devices
* `.col-sm-` Small devices
* `.col-md-` Medium
* `.col-lg-` Large
* `.col-xl-` Extra Large


### Text
Display Headings:
* `display-1`: Big Boy
* `display-2`: Big only
* `display-3`: Med
* `display-4`: Smol


`.text-black-50` gives text black color, with 50% opacity
`.bg-dark` Dark theme 
`.bg-secondary` Grey theme

### Table
Adding classes to style things 
`.table`: Basic Styling
`.table-hover`: On hover gets highlighted
`.table-stripped`: Zebra styling
`.table-borderless`: No border on table


### Jumbotron
`jumbotron`: Adds a big grey box
`jumbotron-fluid`: Full width 
