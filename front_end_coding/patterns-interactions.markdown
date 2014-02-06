---
layout: front_end_guide
title: Interactions Pattern
---

Forms, which are styled in 07-interactions.css, should be labeled with fieldsets and legends. Every submit button should be marked up with a `<p class="submit">`. On some forms there are cancel buttons, so apply the class to the input (`<input class="cancel"...>`) and to that paragraph's classes (`<p class="cancel submit">`).

Form controls are inline elements, which means they have to be wrapped in block level elements.

###### Rules

We generally want forms set up as [definition lists](http://www.w3schools.com/tags/tag_dl.asp) (`<dl>`) because the [term](http://www.w3schools.com/tags/tag_dt.asp) (`<dt>`) and [definition](http://www.w3schools.com/tags/tag_dd.asp) (`<dd>`) structure corresponds nicely to the typical `<label>Label</label> <input>` structure of a form. We use `<dt>` for the label and `<dd>` for the input, and a `<dt>` can contain more than one `<dd>`. However, since a `<dl>` can only contain `<dt>` and `<dd>` as top-level elements, the form tag itself cannot come inside the definition list, nor can other elements such as paragraphs or linebreaks. That's okay, though -- we take care of the forms' presentation with CSS.   

Some forms cannot be logically structured as terms and definitions. As a last resort, these can be structured as paragraphs and can include linebreaks.

### XHTML diagram

The following diagram is adapted from the new work form.

<ol class="diagram">
<li><code>&lt;form class="verbose post"&gt;</code>
<ol>
<li><code>&lt;p class="required notice"&gt;* Required information&lt;/p&gt;</code></li>
<li><code>&lt;fieldset&gt;</code>
<ol>
<li><code>&lt;legend&gt;Tags&lt;/legend&gt;</code></li>
<li><code>&lt;h3 class="landmark heading"&gt;Tags&lt;/h3&gt;</code></li>
<li><code>&lt;p class="note"&gt;Tags are comma separated, 100 characters per tag.&lt;/p&gt;</code></li>
<li><code>&lt;dl&gt;</code>
<ol>
<li><code>&lt;dt class="required"&gt;</code>
<ol>
<li><code>&lt;label&gt;Rating*&lt;/label&gt;</code></li>
</ol></li>
<li><code>&lt;dd class="required"&gt;</code><ol>
<li><code>&lt;select&gt;</code>
<ol>
<li><code>&lt;option&gt;Not Rated&lt;/option&gt;</code></li>
<li><code>&lt;option...</code></li>
</ol></li>
</ol></li>
<li><code>&lt;dt class="required"&gt;</code>
<ol>
<li><code>&lt;label&gt;Archive Warning*&lt;/label&gt;</code></li>
</ol></li>
<li><code>&lt;dd class="required"&gt;</code>
<ol>
<li><code>&lt;fieldset&gt;</code>
<ol>
<li><code>&lt;ul&gt;</code>
<ol>
<li><code>&lt;li&gt;</code> <code><span>&lt;input type="checkbox"&gt;</span> <span>&lt;label&gt;Choose Not To Use Archive Warnings&lt;/label&gt;</span></code></li>
<li><code>&lt;li...</code></li>
</ol></li>
</ol></li>
</ol></li>
<li><code>&lt;dt class="required"&gt;</code>
<ol>
<li><code>&lt;label&gt;Fandoms*&lt;/label&gt;</code></li>
</ol></li>
<li><code>&lt;dd class="required"&gt;</code>
<ol>
<li><code>&lt;input type="text"&gt;</code></li>
<li><code>&lt;p class="footnote"&gt;This is information about the field.&lt;/p&gt;</code></li>
</ol></li>
</ol></li>
</ol></li>
<li><code>&lt;fieldset&gt;</code>
<ol>
<li><code>&lt;legend&gt;</code></li>
<li><code>&lt;h3 class="landmark heading"...</code></li>
<li><code>&lt;dl&gt;</code>
<ol>
<li><code>&lt;dt...</code></li>
<li><code>&lt;dd...</code></li>
</ol></li>
</ol></li>
<li><code>&lt;fieldset&gt;</code>
<ol>
<li><code>&lt;legend&gt;Post&lt;/legend&gt;</code></li>
<li><code>&lt;h3 class="landmark heading"&gt;Post&lt;/h3&gt;</code></li>
<li><code>&lt;ul class="actions"&gt;</code>
<ol>
<li><code>&lt;li&gt;</code>
<ol>
<li><code>&lt;input type="submit"&gt;</code></li>
</ol></li>
<li><code>&lt;li...</code></li>
</ol></li>
</ol></li>
</ol></li>
</ol>
