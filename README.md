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

You also can add gutters between columns. Gutter size must be specified. 
