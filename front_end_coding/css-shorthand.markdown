---
layout: front_end_guide
title: CSS Shorthand
---
On the Archive, we use CSS shorthand. This means we combine properties to make shorter rules. It's an efficient way to code and it's easy to learn with a bit of practice. Without shorthand, our code might look like this:

```
background-color: #ffffff;
background-image: url("../images/example.jpg");
background-repeat: no-repeat;
background-attachment: scroll;
background-position: left top;
```

But **with** shorthand, we can create the same style using only this:

<code>background: <span title="color">#fff</span> <span title="image">url("../images/example.jpg")</span> <span title="repeat">no-repeat</span><span title="scroll is default value"> </span><span title="position">left top</span>;	
</code>

Notice that all these properties begin with background. You can combine properties that have a common prefix.

### Syntax order

Shorthand must be written in a specific order, with the property values separated by a single space. The shorthand `font` property is written like this: `font-style font-variant font-weight font-size line-height font-family`.

So to set a heading's font property, we would write: <code>h5 { font: <span title="style">italic</span> <span title="variant">small-caps</span> <span title="weight">100</span> <span title="size">2em</span> <span title="line-height">1.2</span> <span title="family">Georgia</span>, <span title="family fallback alternative">serif</span>; }</code>

Commas denote alternative values. In the previous example, the comma says the value for `font-family` should be `serif` if `Georgia` is not available.

Shorthand for [box dimensions](http://www.w3.org/TR/CSS2/box.html), like `margin` and `padding`, are written *around the clock*. That means top, right, bottom, left: <code>margin: <span title="top">1em</span> <span title="right">2em</span> <span title="bottom">3em</span> <span title="left">4em</span>;</code>

### Assumed values

In CSS we try to only write what is *different* from the default and inherited values. If your value is normal (the default), you can leave it out and the parser will assume you wrote it, just like it assumes <code>html body #main ol.work.index li<strong>.blurb</strong> h5 a<strong>.tag</strong></code> is the same as `.blurb .tag`.

Similarly, if your paired values are identical, you only need to write one of them. If `margin-top` and `margin-bottom` are the same, and `margin-right` and `margin-left` are the same, you can write: <code>margin: <span title="top and bottom">2em</span> <span title="right and left">3em</span>;</code>.

If the values are the same all the way round the clock, you can write: `margin: 2em;`.

Hex codes have paired values: `#990000` is 99, 00, 00. So you can let the parser assume the second value in each pair and write `#900`.

But there are some values you must always declare:

				<dl>
					<dt>border</dt>
					<dd>width, style (if you don't declare a color it assumes the font colour)</dd>
					<dd><code>border: 1px solid;</code></dd>
					<dt>font</dt>
					<dd>size, family</dd>
					<dd><code>font:<span title="font-size">1em</span> <span title="font-family">serif</span>;</code></dd>
				</dl>

### Combining selectors

If several elements in a structure have the same rules, we can combine the selectors using a comma, which says we mean selector one *and* selector two.

```
.blurb .warning { margin: 1em; }
.blurb .rating { margin: 1em; }
```

can be reduced to <code>.blurb .rating<strong>,</strong> .blurb .warning { margin: 1em; }</code>

In our stylesheets, we only combine selectors within a supertype class (e.g. `.blurb` and `.navigation`) section. We don't use 'streamlining' software to find and combine all selectors with the same rules. This makes code really hard to maintain, and can destroy a complex cascade design, so make sure you don't ever do this.

### Resources

Following are links to the shorthand specs for the properties you'll see most often in our code:
				
* [background](http://www.w3.org/TR/CSS2/colors.html#prop-def-background) 
* [border](http://www.w3.org/TR/CSS2/box.html#border-shorthand-properties)
* [font](http://www.w3.org/TR/CSS2/fonts.html#font-shorthand)
* [list-style](http://www.w3.org/TR/CSS2/generate.html#list-style)
* [margin](http://www.w3.org/TR/CSS2/box.html#margin-properties)
* [padding](http://www.w3.org/TR/CSS2/box.html#padding-properties)

If the specs don't make sense to you, try reading the W3Schools version:

* [background school](http://www.w3schools.com/css/css_background.asp)
* [border school](http://www.w3schools.com/css/css_border.asp)
* [font school](http://www.w3schools.com/css/css_font.asp)
* [list-style school](http://www.w3schools.com/css/css_list.asp)
* [margin school](http://www.w3schools.com/css/css_margin.asp)
* [padding school](http://www.w3schools.com/css/css_padding.asp)