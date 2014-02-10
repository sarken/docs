---
layout: front_end_guide
title: Coding Standards
---
This is a guide to the specifications and formatting standards used in our front-end code, which involves a CSS cascade and a consistent HTML framework used across many of our pages. Our standards help us write code that is super-accessible and as easily maintainable as possible, so if you're committing code, please make sure it follows these standards.

* [XHTML specifications](#xhtml-specifications)
    * [Content-type/charset](#xhtml-specifications-content-type-charset)
    * [Frequently used fragments](#xhtml-specifications-frequently-used-fragments)
    * [XHTML identifiers](#xhtml-specifications-xhtml-identifiers)
        * [Ids](#xhtml-specifications-xhtml-identifiers-ids)
        * [Classes](#xhtml-specifications-xhtml-identifiers-classes)
        * [Our XHTML identifier naming conventions](#xhtml-specifications-xhtml-identifiers-naming-conventions)
* [CSS specifications](#css-specifications)
    * [Units of measurement](#css-specifications-units-of-measurement)
        * [Screen](#css-specifications-units-of-measurement-screen)
        * [Print](#css-specifications-units-of-measurement-pring)
    * [Our CSS formatting conventions](#css-specifications-formatting-conventions)

<h3 id="xhtml-specifications">HTML specifications</h3>

All of our pages are written in [XHTML 1.0](http://www.w3.org/TR/xhtml1/) (Strict), which is a cleaner, stricter version of HTML that separates content from presentation. Our pages use `<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">` as their `DOCTYPE` declaration.

Writing in XHTML 1.0 (Strict) means:

* All markup must be written in lowercase
* All tags must be closed
  * Empty tags are closed within the tag, e.g. `<br />`
  * Non-empty tags have a corresponding closing tag, e.g. `<p>This is a paragraph.</p>`
* All tags must be properly nested
* No [deprecated elements](http://webdesign.about.com/od/htmltags/a/bltags_deprctag.htm) are included

While our use of the <abbr title="Accessible Rich Internet Applications">ARIA</abbr> `role` attribute means our pages will not validate, we still recommend checking your work with [the W3C Markup Validation Service](http://validator.w3.org") to catch any mistakes.

<h4 id="xhtml-specifications-content-type-charset">Content-type/charset</h4>

The Archive uses the UTF-8 character set: `<meta http-equiv="Content-Type" content="text/html;charset=utf-8" />`

<h4 id="xhtml-specifications-frequently-used-fragments">Frequently used fragments</h4>

There are some patterns that appear in many places throughout the Archive. There are diagrams of these recurring patterns available in our [Patterns Index](patterns).

<h4 id="xhtml-specifications-xhtml-identifiers">XHTML identifiers</h4>

Identifiers are attributes that add meaning to an XHTML element by providing more information about the element's function. Identifiers come in two varieties, `class` and `id`. An element can have one, both, or neither type of identifier.

<h5 id="xhtml-specifications-xhtml-identifiers-ids">Ids</h5>

The `id` identifier assigns a name to an element. The name can only be used once per document, and each element can only have one `id`.

Stylesheets, scripts, and user agents can referece an elements by its `id`. An `id` can also serve as an anchor in a hyperlink or as a name for a declared `object` element.

<h5 id="xhtml-specifications-xhtml-identifiers-classes">Classes</h5>

A `class` identifier assigns a name to an element, but `class` names can be used multiple times per document and any element can have multiple `class` names, with each name separated by a single space: `<div class="preface group">This div has the names group and preface.</div>`.

<h5 id="xhtml-specifications-xhtml-identifiers-naming-conventions">Our identifier naming conventions</h5>

Class names should be short, lowercase English (U.S.) words in common usage. They should describe the function, not presentation, of the element to which they are applied. There is more information available in the [Classes document](classes.html).

An `id` name can and should be more complex to ensure that it only appears once per document. We use underscores to separate the words and numbers in the `id`: `<form id="work_filters">` or `<li id="work_1234">`

<h3 id="css-specifications">CSS specifications</h3>

We use aproximately 30 external stylesheets written primarily to [CSS 2.1 Specifications](http://www.w3.org/TR/CSS2/), although we do permit the use of CSS3 to provide non-essential formatting frills, such as box shadows, text shadows, and gradients. We do not use inline styles.

Before submitting any code, it is always a good idea to check your CSS with [the W3C CSS validation service](http://jigsaw.w3.org/css-validator/).

<h4 id="css-specifications-units-of-measurement">Units of measurement</h4>

Since Archive users and visitors browse the site with a variety of technologies, needs, and settings, we want our layout to be as flexible as possible. Using the right units of measurement in the right context helps us accomplish that.

<h5 id="css-specifications-units-of-measurement-screen">Screen</h5>

We use relative measurements to specify all text and most element sizes on our screen layout.

We set our text size using [ems](em-scale.html) and unitless line height. We also use ems to set padding, margins, and widths and heights for other elements.

However, there are times when using an absolute measurement is the best option. For example, we use pixels in instances where an element's `margin` is dependent on the size of an image (e.g., on top of collection profiles).

<h5 id="css-specifications-units-of-measurement-print">Print</h5>

We have a separate stylesheet that controls the appearance of pages printed from the Archive. Text in our print stylesheet is sized using points.

<h4 id="css-specifications-formatting-conventions">Our CSS formatting conventions</h4>

Since our stylesheets are edited by multiple coders, we have developed a house style that will allow us to easily read, track changes to, and avoid mistakes in our styles.

A declaration block written for the Archive should be formatted with:

* Muliple selectors on the same line, separated by a comma and a single space
* The opening curly brace on the same line as the selector, preceded by a single space
* Each property indented and on a new line  
  * CSS 2.1 properties indented by two spaces
  * CSS3 properties listed last and indented by four spaces
* A space between the colon and the property value
* A semicolon at the end of each property, including the last one
* The closing curly brace on a new line, not indented
* A single blank line after each declaration block
* A zero preceding any decimal value that is less than 1 (e.g. `0.643em`)

Here is an example:

```css
#header ul.primary {
  float: none;
  margin: auto;
  background: #900 url(/images/skins/textures/tiles/red-ao3.png);
  border-bottom: 2px solid #700;
  padding: 0.25em 120px;
    box-shadow: inset 0 -5px 10px rgba(0,0,0,0.5);
}
    
#header .primary a, #header .primary .current, #header .primary input, #header .search input {
  border-color: #a00;
  border-bottom-color: #400;
}
```
