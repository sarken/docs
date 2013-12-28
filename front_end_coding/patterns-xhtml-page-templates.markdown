---
layout: front_end_guide
title: XHTML Page Templates
---
<ol class="diagram">
<li>body
<ol>
<li>ul #skiplinks</li>
<li>div #header</li>
<li class="emphasise">div #main</li>
<li>div #footer</li>
</ol></li>
</ol>

The individual pages on the Archive are contained within the division `#main`.

Some pages (user home, collection home, tag home, admin home) have a dashboard, which by default we display as a sidebar.

<ol class="diagram">
<li>body
<ol>
<li>ul #skiplinks</li>
<li>div #header</li>
<li>div #dashboard</li>
<li class="emphasise">div #main	.dashboard</li>
<li>div #footer</li>
</ol></li>
</ol>

Each page follows the same basic structure and order. The structure is commented in the views. Each section is announced by a heading, although many of these headings are not displayed in the Archive default style; these are landmarks.

```html
<!--Descriptive page name and system messages, descriptions, and instructions.-->
<h2> </h2>

<!--Subnavigation, sorting and actions.-->
<h3 class="landmark"> </h3>

<!--main content-->
<h3 class="landmark"> </h3>

<!--Subnavigation, sorting and actions.-->
<h3 class="landmark"> </h3>
```

Here's a brief look at the structure of a a filterable work index, like the [work index for The X-Files](http://archiveofourown.org/tags/The%20X-Files/works):

<ol class="diagram">
<li>#main
<ol>
<li>h2</li>
<li>h3 .landmark</li>
<li>ul .navigation
<ol>
<li>li <span>a</span></li>
<li>li <span>span .current</span></li>
</ol>
</li>
<li>h3 .landmark</li>
<li>ol .work index
<ol>
<li>blurb</li>
<li>blurb</li>
<li>blurb</li>
<li>blurb...</li>
</ol>
</li>
<li>form .filters #work_filters
<ol>
<li>h3 .landmark</li>
<li>fieldset
<ol>
<li>legend</li>
<li>dl .filters
<ol>
<li>dt .landmark</li>
<li>dd .submit
<ol>
<li>input</li>
</ol>
</li>
<li>dt...</li>
<li>dd...</li>
<li>dt .landmark</li>
<li>dd .submit
<ol>
<li>input</li>
</ol>
</li>
</ol>
</li>
</ol>
</li>
</ol>
</li>
<li>
</li>
<li>ol .pagination
<ol>
<li>li .previous
<ol>
<li>a</li>
</ol>
</li>
<li>li
<ol>
<li>span .current</li>
</ol>
</li>
<li>li
<ol>
<li>a</li>
</ol>
</li>
<li>li...</li>
<li>li .next
<ol>
<li>a</li>
</ol>
</li>
</ol>
</li>
</ol>
<li>div .clear</li>
</ol>

You can look at some of the more commonly used structures as diagrams, and look at [the blurb in detail](case-study-the-blurb).
