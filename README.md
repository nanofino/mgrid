Modern Grid (mgrid)
=====

Overview
---
This is a simple CSS3-based grid framework. It relays on the new pseudo-selectors to automatically determinates the grid's equal columns width, depending on the amount of columns. 
As a modern approach to laying out a grid, it is intended for modern browsers that support CSS3, so it doesn't work correctly on browsers like IE6 or IE7 by itself. Javascript workarounds are needed (and provided) in order to be supported by old browsers. Those are:
+ [Selectivzr.js](http://selectivizr.com) (provides suppoort for CSS3 pseudo-selectors to IE6-IE8)
+ [jQuery](http://jquery.com) (needed by Selectivr.js) 

How to use it:
---
You don't need to specificate the amount of columns to determinate the column's width. 
All you have to do is set a container and apply the class "cols" to it, and fill it with columns, which must have the class "column".

For example, for a 4-column layout:
```html
<div class="cols">
    <div class="column">Column 1</div>
    <div class="column">Column 2</div>
    <div class="column">Column 3</div>
    <div class="column">Column 4</div>
</div>
```
###Adding Gutters
You also can add gutters between columns. Gutter size must be specified on the CSS, and the column's content should be wrapped by an element with class "colContent". Also, the column container should have the class "gutters" added.
The HTML markup should be like this:
```html
<div class="cols gutters">
    <div class="column">
        <div class="colContent">Column 1</div>
    </div>
    <div class="column">
        <div class="colContent">Column 2</div>
    </div>
    <div class="column">
        <div class="colContent">Column 3</div>
    </div>
    <div class="column">
        <div class="colContent">Column 4</div>
    </div>
</div>
```
The gutter's width is specified in the *mgrid.css* file, at its bottom, and look like this:
```CSS
.cols.gutters {
	margin-left: -1em;		/* fallback for browsers not supporting rems values */
	margin-left: -1rem;	/* normalized gutters value for nested columns, no matter differents font-size values */ 
}
.cols.gutters  .colContent {
	margin-left: 1em;		/* fallback for browsers not supporting rems values */
	margin-left: 1rem;	/* normalized gutters value for nested columns, no matter differents font-size values */ 
}
```
In this case, the gutter is about **1rem** (or **1em** for those browsers that not support the 'rem unit').
Both declarations must have the same value, althought **_.cols.gutters_** must have it in negative, and **_.cols.gutters .colContent_** in positive.

It could be done with just one declaration (margin-left: 1rem for .colContent, and overrided to 0 for the first-child) but that approach makes the first column wider.

Finally
___

This grid is free to use and modified as you need. If you use it, be sure to let me know how does it work. If you find a bug, or a come up with an enhancement, drop me a line.
Also, I'd love to see it in action, so don't forget to send me the URL where it is used.

-by Hernan Fino
