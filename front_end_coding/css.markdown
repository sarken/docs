---
layout: front_end_guide
title: What is CSS
---
Cascading Stylesheets (CSS) tell a browser how to display our XHTML document. We write a list of rules describing the color of the text, the size of the boxes -- what goes where and what it looks like.

To write a CSS document, conceptually, we examine the structure of an HTML document:

```html
  <body>
    <div id="header">
      <h1>My Page Title</h1>
      <ul class="navigation">
        <li> <a href="...">site section one</a> </li>
        <li> <a href="...">site section two</a> </li>
      </ul>
    </div>
    <div id="main">
      <p>My content goes here</p>
      <span class="navigation"> <a href="...">home</a> </span>
    </div>
    <div id="footer">
      <p>My page by me!</p>
    </div>
</body>
```

...and then we lay out our CSS document in the same order: 


```css
body { 
  property: value;
}

#header {
  property: value;
}

#header h1 { 
  property: value;
}

ul.navigation { 
  property: value;
}

#main { 
  property: value;
}

#main p { 
  property: value;
}

#footer { 
  property: value;
}
```

HTML documents are like tupperware on a shelf: boxes nested inside each other. Everything **nested** inside the body tag **inherits** the properties and values assigned to body, unless you say different. Everything inside `#main` inherits the properties of `body` and `#main`, and so on. CSS then, cascades down the page, sort of like champagne filling a pyramid of glasses.

### CSS terms

A single CSS **rule set** is made up of the following parts:

```css
selector { 
  property: value;
}
```

A property must always be paired with a value to form a valid **declaration**. A single rule set can have multiple selectors separated by commas or multiple declarations separated by semi-colons.

#### Selectors

A **selector** is the part of the rule that says which elements are being styled. A rule set can have multiple selectors to make it apply to multiple elements, and different types of selectors can be combined in order to select an element only when it appears within a specific context.

##### ID selectors

Some elements that are used only once per page have unique names that are given to them with the HTML `id` attribute, like `<div id="header">`. To select an element by its `id`, use a hash sign in front of the element's `id` value.

```css
#header {
  property: value;
}
```

##### Class selectors

For something used more than once, we may assign a class, or many classes. A class says this is a type, not a unique thing. Our example HTML has both `<ul class="navigation">` and `<span class="navigation">`. We could target both of those elements at once using their shared `class` value. 

To select elements by a `class` attribute, use a period in front of the desired `class` value.

```css
.navigation {
  property: value;
}
```

##### Type selectors

Type selectors apply a style to a type of HTML element. To select all elements that are a certain type, use the element name as the selector.

```css
p {
  property: value;
}
```

##### Using selectors

Looking again at the example HTML and CSS documents, notice that the selector in a style rule is actually a *path*. You can select every paragraph everywhere using just a type selector:

```css
p { 
  property: value;
}
```

Or you can specify only certain paragraphs, in certain places, by combining different kinds of selectors:

```css
p {
  property: value;
}

body #footer p { 
  property: value;
}
```

#### Properties and values

Think of each selector as a box. We can make it stack up, give it a background color (or an image or both), a border, and we can give that border a color and a thickness and a style. We can decide how big each box is and much blank space is going to be around it (`margin`) and inside it (`padding`). We can position (float, top, left) each box on the page. We can make the text in the box a particular size, color, font, and make it bold or italic; we can align it to the left or the right or center it. We can do (almost) anything!
				
##### Values

On the Archive, we primarily use hex codes to define colors. Hex codes are a set of six letters (a-f) and digits (0-9) that make up a color. `#000000` is black. `#ffffff` is white. Everything else is somewhere in between.

<ol class="diagram">
<li>Black (#000000): <span style="display:inline-block; width:1em; height:1em; background:1px solid; background:#000; margin:auto; padding:0;" title="#000"></span></li>
<li>White (#ffffff): <span style="display:inline-block; width:1em; height:1em; background:1px solid; background:#fff; margin:auto; padding:0;" title="#fff"></span></li>
<li>Red (#990000): <span style="display:inline-block; width:1em; height:1em; background:1px solid; background:#900; margin:auto; padding:0;" title="#900"></span></li>
</ol>

We use [ems](em-scale.html) as the general unit of measurement. 1 em is 100% of your font size; if your font size is 16px, 1 em is 16px. Since ems are a scalable measurement, if your visitor needs to zoom in or scale up the text, your layout is less likely to go horribly wrong.

1 em square: <span style="display:inline-block; width:1em; height:1em; background:1px solid; background:#000; margin:auto; padding:0;"></span>

###### Block and inline

HTML elements come in two flavosrs: block-level and inline.

<ol class="diagram" title="block level HTML elements stacking up">
<li>&lt;ul&gt;
<ol>
<li>&lt;li&gt; block level elements &lt;/li&gt;</li>
<li>&lt;li&gt; are like building blocks &lt;/li&gt;</li>
<li>&lt;li&gt; they stack up one underneath the other &lt;/li&gt;</li>
</ol></li>
</ol>

<p class="diagram">Elements like <span>&lt;a href="http://..."&gt;<a href="">links</a>&lt;/a&gt;</span> and <span>&lt;em&gt;<em>emphasis</em>&lt;/em&gt;</span> run along in a line, like text does.</p>

Elements are either block or inline by default, but with CSS we can decide how we want to display *every single element* on the screen. So we can make the list items (`<li>`) of an unordered list (`<ul>`), which is a block containing a stack of blocks, into a line of elements very easily, with the rule `ul li { display: inline; }`

<ol class="diagram" title="block level HTML elements displayed inline">
<li>&lt;ul&gt;
<ol>
<li style="display:inline;">&lt;li&gt; css &lt;/li&gt;</li>
<li style="display:inline;">&lt;li&gt; controls &lt;/li&gt;</li>
<li style="display:inline;">&lt;li&gt; presentation &lt;/li&gt;</li>
</ol></li>
</ol>
				
Think of each selector as a box. We can make it stack up, give it a background color (or an image or both), a border, and we can give that border a color and a thickness and a style. We can decide how big each box is and much blank space is going to be around it (margin) and inside it (padding). We can position (float, top, left) each box on the page. We can make the text in the box a particular size, color, font, and make it bold or italic or asscaps; we can align it to the left or the right or center it. We can do anything! (Almost anything.)
				
### Resources
* [CSS Terms and Definitions](http://www.impressivewebs.com/css-terms-definitions/)
* [ProCSSor CSS Prettifier](http://procssor.com)
* [W3C CSS Validator](http://jigsaw.w3.org/css-validator/)
* [CSS 'default' styles](http://www.w3.org/TR/CSS21/sample.html)