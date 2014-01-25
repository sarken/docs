---
layout: front_end_guide
title: Actions Pattern
---
Actions are links and form inputs, which we style to look like buttons.

It's a very loose pattern, but it's normally a list of links. On most pages, there is an unordered actions list straight after the `h2` page heading. Actions can show up anywhere, however, in any group, zone, region, or interaction.

The actions styles are declared in [the style sheet named 08-actions.css](https://github.com/otwcode/otwarchive/blob/master/public/stylesheets/site/2.0/08-actions.css). They are a [supertype](supertype).

### Subtypes of actions

* .navigation
  * .landmark
  * #skiplinks
  * .current
  * .pagination
* .sorting
* .action
* .submit
* input[type="submit"]
* .cancel
* .close
* .delete
* button

### Rules

Actions can be any element that contains one or more actions. While actions frequently appear in groups marked up as unordered lists (`<ul class="actions">`), single actions are often seen inside paragraphs (`<p>`) or descriptions (`<dd>`) with the `action` class applied to the containing element (rather than the link or input).

Nested actions blocks have the class `secondary`, which is a general modifier.

Only `simple` forms should be included inside actions blocks.

### XHTML Diagram

<ol class="diagram">
<li><code>&lt;ul class="navigation actions" role="navigation"&gt;</code>
<ol>
<li><code>&lt;li&gt;</code>
<ol>
<li><code>&lt;a&gt;</code></li></ol>
</li>
<li><code>&lt;li&gt;</code>
<ol>
<li><code>&lt;span class="current"&gt;</code></li>
</ol></li>
<li><code>&lt;li aria-haspopup="true"&gt;</code>
<ol>
<li><code>&lt;a&gt;</code></li>
<li><code>&lt;ul class="secondary"&gt;</code>
<ol>
<li><code>&lt;li&gt;</code>
<ol>
<li><code>&lt;a&gt;</code></li>
</ol></li>
<li><code>&lt;li&gt;</code>
<ol>
<li><code>&lt;a&gt;</code></li>
</ol>
</li></ol>
</li>
</ol>
</li>
<li><code>&lt;li&gt;</code>
<ol>
<li><code>&lt;a&gt;</code></li>
</ol>
</li></ol>
</li>
</ol>

### Actions and landmark headings

Sometimes actions blocks are announced by a landmark heading. This is a case-by-case decision and must not be done reflexively, only where it is properly useful, like where there are lots of different kinds of actions blocks grouped, or where a user is probably going to load a page and go directly to a specific action. So, in layout, you can't rely on an actions block being directly preceded by a heading.

### ARIA roles and states

As well as Archive roles and states, actions can have [ARIA roles](http://www.w3.org/TR/wai-aria/roles) and states.

<dl>
<dt><a href="http://www.w3.org/TR/wai-aria/roles#navigation">role="navigation"</a></dt>
<dd>a block of mostly links that take you to other places</dd>
<dt><a href="http://www.w3.org/TR/wai-aria/roles#menu">role="menu"</a></dt>
<dd>a block of mostly form buttons (like submit, select, destroy)</dd>
<dt><a href="http://www.w3.org/TR/wai-aria/roles#button">role="button"</a></dt>
<dd>a single button in a navigation block, or a button on its own</dd>
<dt><a href="http://www.w3.org/TR/wai-aria/states_and_properties#aria-haspopup">aria-haspopup="true"</a></dt>
<dd>has a hidden secondary block</dd>
</dl>