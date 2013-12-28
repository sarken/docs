---
layout: front_end_guide
title: Index Pattern
---
Index is a very general class of list. You'll most often see it containing blurbs, or as the content in a listbox, but it isn't restricted to those. Index has very few rules; it's a flexible grouping class. 

It doesn't have its own style sheet, but index styles are declared in [the style sheet named 10-types-groups.css](https://github.com/otwcode/otwarchive/blob/master/public/stylesheets/site/2.0/10-types-groups.css). Index is the most used example of the polyvalent "[types](types) or [states](modifiers) of [groups](supertypes)."

### Index HTML structure

An index can be any kind of list.

* dl.index
* ol.index
* ul.index

You can **never** have **any** other kind of index.

#### dl.index

`dl.index` is sometimes used to display paired data (e.g. on [a translated news post](http://archiveofourown.org/admin_posts/148)), but it most frequently functions as the brief blurb pattern, like on a user's challenge assignments page.

<ol class="diagram">
<li>&lt;dl class="assignment index group"&gt;
<ol>
<li>&lt;dt&gt;
<ol>
<li>&lt;a&gt;Assignment link</li>
</ol>
</li>
<li>&lt;dd&gt;
<ol>
<li>&lt;ul class="navigation actions" role="menu"&gt;
<ol>
<li>&lt;li&gt;
<ol>
<li>&lt;a role="button"&gt;Fulfill</li>
</ol>
</li>
<li>&lt;li&gt;
<ol>
<li>&lt;a role="button"&gt;Default</li>
</ol>
</li>
</ol>
</li>
</ol>
</li>
<li>&lt;dt&gt;
<ol>
<li>&lt;a&gt;Assignment link</li>
</ol>
</li>
<li>&lt;dd&gt;
<ol>
<li>&lt;a&gt;Work link
</li>
<li>&lt;dl class="stats"&gt;
<ol>
<li>&lt;dt&gt;</li>
<li>&lt;dd&gt;</li>
</ol>
</li>
</ol>
</li>
</ol>
</li>
</ol>

#### ol.index and ul.index

