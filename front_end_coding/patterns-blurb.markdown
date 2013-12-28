---
layout: front_end_guide
title: Blurb Design Pattern
---
<ol class="diagram">
<li>landmark heading level 3 "list of works" <code>&lt;h3 class="landmark heading"&gt;Listing Works&lt;/h3&gt;</code></li>
<li>list container work index <code>&lt;ul class="work index group"&gt;</code>
<ol>
<li class="emphasize">list item work blurb <code>&lt;li class="work blurb group"&gt;</code>
<ol>
<li>division header module <code>&lt;div class="header module"&gt;</code>
<ol>
<li>heading level 4 title link by user link <code>&lt;h4 class="heading" title="title"&gt;</code></li>
<li>heading level 5 fandom tag link <code>&lt;h5 class="fandoms heading" title="fandom"&gt;</code></li>
<li>unordered list of required tags <code>&lt;ul class="required-tags"&gt;</code>
<ol>
<li>list item with rating symbol<code>&lt;li&gt;...&lt;span class="rating...</code></li>
<li>list item with warnings symbol<code>&lt;li&gt;...&lt;span class="warnings...</code></li>
<li>list item with category symbol<code>&lt;li&gt;...&lt;span class="category...</code></li>
<li>list item with work status symbol<code>&lt;li&gt;...&lt;span class="iswip...</code></li>
</ol>
</li>
<li>paragraph datetime <code>&lt;p class="datetime"&gt;</code></li>
</ol>
</li>
<li>landmark heading level 6 "tags" <code>&lt;h6 class="landmark heading"&gt;Tags&lt;/h6&gt;</code></li>
<li>unordered list of tags <code>&lt;ul class="tags commas"&gt;</code>
<ol>
<li>list item(s) with warnings tags <code>&lt;li class="warnings"&gt;&lt;a class="tag"...</code></li>
<li>list item(s) with relationship tags (if any) <code>&lt;li class="relationships"&gt;&lt;a class="tag"...</code></li>
<li>list item(s) with character tags (if any) <code>&lt;li class="characters"&gt;&lt;a class="tag"...</code></li>
<li>list item(s) with additional tags (if any) <code>&lt;li class="freeforms"&gt;&lt;a class="tag"...</code></li>
</ol>
</li>
<li>landmark heading level 6 "summary" <code>&lt;h6 class="landmark heading"&gt;Summary&lt;/h6&gt;</code></li>
<li>blockquote of summary <code>&lt;blockquote class="userstuff summary" title="summary"&gt;</code></li>
<li>landmark heading level 6 "series" <code>&lt;h6 class="landmark heading"&gt;Series&lt;/h6&gt;</code></li>
<li>unordered list of series <code>&lt;ul class="series"&gt;</code>
<ol>
<li>list item(s) with series <code>&lt;li&gt;Part &lt;strong&gt;X&lt;/strong&gt; of &lt;a href="..."&gt;Series Title&lt;/a&gt;&lt;/li&gt;</code></li>
</ol>
</li>
<li>definition list of stats <code>&lt;dl class="stats" title="stats"&gt;</code>
<ol>
<li>definition list property: value pairs <code>&lt;dt&gt;Words:&lt;/dt&gt;&lt;dd&gt;151&lt;/dd&gt;...</code></li>
</ol>
</li>
</ol>
</li>
<li>next list item work blurb</li>
</ol>
</li>
</ol>