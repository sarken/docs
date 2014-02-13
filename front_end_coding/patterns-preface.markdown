---
layout: front_end_guide
title: Preface Pattern
---
Preface groups together user notes about a work, collection, or challenge. Modules that are grouped in preface include: summary, notes, end notes, FAQ, rules, about, description. On a work page, preface is inside `#workskin`, so it can be styled in work skins as well as site skins.

The preface style is declared in [14-group-preface.css](https://github.com/otwcode/otwarchive/blob/master/public/stylesheets/site/2.0/14-group-preface.css).

* [Rules](#rules)
* [Quick reference](#quick-reference)
* [XHTML diagram](#xhtml-diagram)

<h3 id="rules">Rules</h3>

A preface can be any block containing a child that can contain these blocks: `h1—6`, `p`, `div`, `ul`, `ol`, `dl`, `blockquote`. Normally it's a `div`.

A preface always contains a `blockquote.userstuff`, although the `blockquote` may be logicked out (e.g. if a work doesn't have a summary or note but does have associations).

A preface can have lots of child modules. You can have a preface with restricted children: `table.preface`, `ol`, `ul`, or `dl.preface`, so long as the block children are given the `module` class.

You can never have an inline preface, or a phrase element preface.

<h3 id="quick-reference">Quick reference</h3>

<dl><dt>[...]</dt><dd>always included</dd>
<dt>{...}</dt><dd>sometimes included</dd></dl>

[preface]
	{title heading} {byline heading}
	[block module]
	  [heading] {span actions}[/heading]
	  [blockquote userstuff]
	  {p note} {ul actions}
	[block module]
[/preface]

<h3 id="xhtml-diagram">XHTML diagram</h3>