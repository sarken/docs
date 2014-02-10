---
layout: front_end_guide
title: Actions Pattern
---
Actions are links and form inputs, which we style to look like buttons.

It's a very loose pattern, but it's normally a list of links. On most pages, there is an unordered actions list straight after the `h2` page heading. Actions can show up anywhere, however, in any group, zone, region, or interaction.

The actions styles are declared in [the style sheet named 08-actions.css](https://github.com/otwcode/otwarchive/blob/master/public/stylesheets/site/2.0/08-actions.css). They are a [supertype](supertype).

* [Rules](#rules)
* [XHTML diagram](#xhtml-diagram)
* [Subtypes of actions](#subtypes-of-actions)
* [Actions and landmark headings](#actions-and-landmark-headings)
* [ARIA roles and states](#aria-roles-and-states)

<h3 id="rules">Rules</h3>

Actions can be any element that contains one or more actions. While actions frequently appear in groups marked up as unordered lists (`<ul class="actions">`), single actions are often seen inside paragraphs (`<p>`) or descriptions (`<dd>`) with the `action` class applied to the containing element (rather than the link or input).

Nested actions blocks have the class `secondary`, which is a general modifier.

Only `simple` forms should be included inside actions blocks.

<h3 id="xhtml-diagram">XHTML diagram</h3>

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
</li></ol></li>
<li><code>&lt;li&gt;</code>
<ol>
<li><code>&lt;a&gt;</code></li>
</ol>
</li></ol>
</li>
</ol>

<h3 id="rules">Subtypes of actions</h3>

* `.navigation` actions are the major navigational items in a region. In the header, footer, and dashboard, all actions are `.navigation`. In the main region, `.navigation` actions follow the `h2` page heading (they can also be repeated after all other `#main` content).

* `.landmark` items help users who access the Archive with screen readers skip around on a page. In our default style, landmarks are hidden from view in a way that keeps them accessible to screen readers. Landmarks generally do not have the `actions` class and are more often headings than links.

  * `#skiplinks` are links at the top of the page that let users skip over the navigation and go directly to the main content of the page. (You can learn more about skip links from [WebAIM's "Skip Navigation" Links article](http://webaim.org/techniques/skipnav/).)
  
* `.pagination` actions let users move between pages of like items (e.g. when there are more than 20 works for a particular tag, the blurbs are spread across multiple pages).

* `.sorting` actions rearrange items (e.g. a user can rearrange the works on their statistics page most kudos, fewest hits, and so on).

* `.submit` actions are form input controls (e.g. `<p class="submit actions"><input type="submit"></p>`).

* `.action`

* `.current` is an actions state used to give a visual indication that an action corresponds to the current page and parameters (e.g. the "Bookmarks" navigation action has the `.current` state on the [Fullmetal Alchemist bookmarks index](http://archiveofourown.org/tags/Fullmetal%20Alchemist/bookmarks) and the "Comments" sorting action has the `.current` state when sorting statistics by most or least comments).

* `.cancel`
* `.close`
* `.delete`

* `input[type="submit"]` and `button` are elements rather than classes. Browsers typically style these elements to look like buttons by default, but we override that to make them look like *our* buttons.

<h3 id="actions-and-landmark-headings">Actions and landmark headings</h3>

Sometimes actions blocks are announced by a landmark heading. This is a case-by-case decision and must not be done reflexively, only where it is properly useful, like where there are lots of different kinds of actions blocks grouped, or where a user is probably going to load a page and go directly to a specific action. So, in layout, you can't rely on an actions block being directly preceded by a heading.

<h3 id="aria-roles-and-states">ARIA roles and states</h3>

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