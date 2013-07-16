---
layout: front_end_guide
title: What is Semantic XHTML
---
In our [Coding Standards](coding-standards), we say that with semantic <abbr title="Extensible HyperText Markup Language">XHTML</abbr> and <abbr title="Cascading Style Sheets">CSS</acronym> we separate our content from our presentation. eXtensible HyperText Markup Language and Cascading Style Sheets are flexible, accessible, and logical ways to mark up content for the web.

XHTML has a creed, and that creed is the topic of our next section:

*** "Code what you mean; mean what you code."

The combination of CSS and XHTML separates style from content: the way things **look** from what things **mean**. CSS takes care of how everything looks; XHTML controls what things mean. In this way, you can build consistent, logical documents that can be read on any device, by any user agent, whether that be a screen reader, a palm pilot, a printer, or whatever the *next* gadget might be.

It's *faster and easier* to code correctly, because there is a *process of reasoning* that you can follow. Instead of thinking, oh, this is a heading, so I want it to be on its own line, so I'll put a `<br>` break in and I want it bold and in a bigger font and centred, you can just think, oh, this is `<h1>a heading</h1>`.

So, throw out your `<font>` tags! Release your `<b>bolding</b>`! Deny your layout tables and reject your `<center>purely presentational markup</center>`! All that is for your CSS.

Computers don't understand that `<i>this</i>` word is emphasised but `<i>The Lord of the Rings</i>` is a book unless you tell them that `<em>this</em>` word is emphasised and `<cite>The Lord of the Rings</cite>` is a book.

**** But It Looks Bad!

Once your content is marked up in a consistent, semantic, and logical manner, you can go wild with your presentational CSS. You can change the way your entire site looks by changing a single line in a single document. If you decide you want to put a border around every image, for example, you can just write `img { border: 1px solid black; }`

*** Resources

* [W3School's HTML Reference](http://www.w3schools.com/tags/default.asp) lists all HTML tags and notes which are new to HTML5 and which are deprecated.

* [Added Bytes' HTML Cheat Sheet](http://www.addedbytes.com/cheat-sheets/html-cheat-sheet/) is a one-page printable PDF that lists HTML tags, attributes, and events.