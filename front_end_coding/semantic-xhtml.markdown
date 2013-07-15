---
layout: front_end_guide
title: Semantic XHTML
---
In our [Coding Standards](coding-standards.html), we say that with semantic XHTML and [CSS](css.html) we separate our content from our presentation. eXtensible HyperText Markup Language (XHTML) and Cascading Style Sheets (CSS) are flexible, accessible, and logical ways to mark up content for the web.

### Code What You Mean; Mean What You Code

That's the XHTML creed.

CSS and XHTML separate style from content: the way things **look** from what things **mean**. CSS takes care of how everything looks; XHTML controls what things mean. In this way, you can build consistent, logical documents that can be read on any device, by any user agent, whether that be a screen reader, a palm pilot, a printer, or whatever the *next* gadget might be.

It's *faster and easier* to code correctly, because there is a *process of reasoning* that you can follow. Instead of thinking, oh, this is a heading, so I want it to be on its own line, so I'll put a `<br />` in and I want it bold and in a bigger font and centred, you can just think, oh, this is `<h1>a heading</h1>`.
				
So, throw out your font tags! Release your `<b>bolding</b>`! Deny your layout tables and reject your`<center>purely presentational markup</center>`.

Computers don't understand that `<i>this</i>` word is emphasised but `<i>The Lord of the Rings</i>` is a book unless you tell them that `<em>this</em>` word is emphasised and `<cite>The Lord of the Rings</cite>` is a book.

Once your content is marked up in a consistent, semantic, and logical manner, you can go wild with your presentational CSS. You can change the way your entire site looks by changing a single line in a single document.

### Resources

* [A list of all current HTML tags](http://www.w3schools.com/tags/default.asp)
* [HTML Cheat Sheet PDF](http://www.addedbytes.com/cheat-sheets/html-cheat-sheet/)
* [CSS Cheat Sheet PDF](http://www.addedbytes.com/cheat-sheets/html-cheat-sheet/css-cheat-sheet/)
