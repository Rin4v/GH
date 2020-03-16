# Positioning of blocks in CSS

The techniques for positioning blocks on the screen have evolved considerably in CSS.

CSS has always been used for web page layout, but it has never been very good at it. We first used **tables**, then **floats**, various positioning and inline-block, but all these methods were basically similar to patches, and did not solve some recurring problems such as vertical centering. **Flexbox** has helped us a lot, but it is designed for simpler, one-dimensional layouts, not two-dimensional layouts. In fact, Flexbox and Grid complement each other well and are made to work together. **Grid** is the first CSS module created specifically to solve layout problems.

To give an overview we have :

## The use of `<table>`:

Useful at the very beginning of the Web. Avoid using tables for block positioning at all costs. But if you want to display a real table no problem (newsletter...)

### Details

The HTML element `<table>` allows to represent a set of data expressed on a table in two dimensions.

````HTML
<table>
    <thead>
        <tr>
            <th>Head 1</th>
            <th>Head 2</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Content 1</td>
            <td>Content 2</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td>Footer 1</td>
            <td>Footer 2</td>
        </tr>
    </tfoot>
</table>
````

### Other tags

````HTML
<col>
<colgroup></colgroup>
<caption></caption>
````

## The use of `float`:

Good for some cases but contains problems of incompatibilities between browsers.

### Details

````HTML
<div>
    <h2>Coucou !</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesentium cupiditate sed sequi odit consequatur quasi. Blanditiis facilis porro praesentium in ratione quos, sed, sapiente cum ipsa, nulla sit nesciunt? Dolorum.
    </p>
</div>
````

````CSS
div {
    border: solid red;
    width: 70px;
}

h2 {
    float: right;
}
````

### Other tags

````CSS
div {
    float: left;
    float: right;
    float: none;
    float: inline-start;
    float: inline-end;
    float: inherit;
    float: initial;
    float: unset;
}
````

## The use of `display: flex`:

Also called Flexbox,the flex property is a shortened property that defines the ability of a flexible element to modify its dimensions in order to fill the available space of it's container.
Technique mainly used, a little complicated but really powerful and practical for responsive, compatible with almost all browsers.

### Details

````HTML
<div class="container">
    <p class="item"></p>
    <p class="item"></p>
    <p class="item"></p>
    <p class="item"></p>
    <p class="item"></p>
</div>
````

````CSS
.container {
    display: flex;
    flex-direction: column;
}
````

### Other tags

````CSS
	flex-basis:;
	flex-direction:;
	flex-flow:;
	flex-grow:;
	flex-shrink:;
	flex-wrap:;
	order:;
````

## The use of `display: grid`:

It's the rising star of css positioning, the only problem is that it is not yet compatible with all browsers.

### Details

BASIC !

````HTML
<div class="container">
    <p class="a">1</p>
    <p class="b">2</p>
    <p class="c">3</p>
    <p class="d">4</p>
    <p class="e">5</p>
    <p class="f">6</p>
</div>
````

````CSS
div {
    display: grid;
    grid-template-columns: 100px 100px;
    grid-template-rows : 100px 100px 100px;
}
.a {
    grid-column : 1;
    grid-row : 1;
}
.b {
    grid-column : 2;
    grid-row : 1;
}
.c {
    grid-column : 1;
    grid-row : 2;
}
.d {
    grid-column : 2;
    grid-row : 2;
}
.e {
    grid-column : 1;
    grid-row : 3;
}
.f {
    grid-column : 2;
    grid-row : 3;
}
````

### Other tags

````CSS
    grid-template-areas:;
    grid-template:;
    grid-auto-columns:;
    grid-auto-rows:;
    grid-auto-flow:;
    grid-row-start:;
    grid-column-start:;
    grid-row-end:;
    grid-column-end:;
    grid-area:;
    row-gap:;
    column-gap:;
    grid-gap:;

````

## Resources

* [Example](https://tobiasahlin.com/blog/common-flexbox-patterns/)
* [A complete guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
