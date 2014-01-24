---
layout: front_end_guide
title: XHTML Page Templates
---
Each page on the Archive follows the same basic structure and order. As discussed in the [Front End User Guide](front-end-user-guide), there are four major regions on the Archive, three of which are included on every page. The skip links are not considered a region and are not visible; however, they are included on every page to allow users of some assistive technology to jump directly to the main content, which is contained within `<div id="main">`.

<ol class="diagram">
<li>body
<ol>
<li>ul #skiplinks</li>
<li>div #header</li>
<li class="emphasize">div #main</li>
<li>div #footer</li>
</ol></li>
</ol>

The dashboard is the only region that does not appear on every page. It most often contains navigation specific to users and collection pages, and it generally takes the form of a sidebar on the left of such pages. (It appears beneath the header and above the main content on very small screens and mobile devices.)

<ol class="diagram">
<li>body
<ol>
<li>ul #skiplinks</li>
<li>div #header</li>
<li>div #dashboard</li>
<li class="emphasize">div #main	.dashboard</li>
<li>div #footer</li>
</ol></li>
</ol>

The structure is commented in the views. Each section is announced by a heading, although many of these headings are not displayed in the Archive default style; these are called landmarks. Like the skip links, they are designed to help users of assistive technology jump around on the page.

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

Here's a brief look at the structure of a filterable work index, like the [work index for The X-Files](http://archiveofourown.org/tags/The%20X-Files/works):

<ol class="diagram">
<li>#main
<ol>
<li>h2</li>
<li>h3 .landmark</li>
<li>ul .navigation
<ol>
<li>li <span>a</span></li>
<li>li <span>span .current</span></li>
</ol></li>
<li>h4 .landmark</li>
<li>ol .pagination
<ol>
<li>li .previous <span>a</span></li>
<li>li <span>span .current</span></li>
<li>li <span>a</span></li>
<li>li...</li>
<li>li .next <span>a</span></li>
</ol></li>
<li>h3 .landmark</li>
<li>ol .work index
<ol>
<li>blurb</li>
<li>blurb</li>
<li>blurb</li>
<li>blurb...</li>
</ol></li>
<li>form .filters
<ol>
<li>h3 .landmark</li>
<li>fieldset
<ol>
<li>legend</li>
<li>dl .filters
<ol>
<li>dt .landmark</li>
<li>dd .submit <span>input</span></li>
<li>dt</li>
<li>dd</li>
<li>dt...</li>
<li>dd...</li>
<li>dt .landmark</li>
<li>dd .submit <span>input</span></li>
</ol>
</li>
</ol>
</li>
</ol>
</li>
<li>h4 .landmark</li>
<li>ol .pagination
<ol>
<li>li .previous <span>a</span></li>
<li>li <span>span .current</span></li>
<li>li <span>a</span></li>
<li>li...</li>
<li>li .next <span>a</span></li>
</ol>
</li>
<li>div .clear</li>
</ol>
</li>
</ol>

Other indices on the Archive, such as [a tag's bookmark index](http://archiveofourown.org/tags/The%20X-Files/bookmarks) and [the collections index](http://archiveofourown.org/collections), follow the same pattern. There are also variations of it that don't have filters, such as [the main works index](http://archiveofourown.org/works), or that have filters and appear a dashboard, such as [a user's bookmark index](http://archiveofourown.org/users/testy/bookmarks).