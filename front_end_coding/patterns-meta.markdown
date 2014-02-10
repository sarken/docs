---
layout: front_end_guide
title: Meta Pattern
---

Meta is a definition list in a wrapper div. We use meta in places such as the start of a work, a series listing, or a user profile. It shows metadata: all the tags, associations, and stats we hold on that object. Sometimes it includes a brief note, but normally it's tags and stats and status type data.

Meta is part of the group [supertype](supertype) and is styled in [12-group-meta.css](https://github.com/otwcode/otwarchive/blob/master/public/stylesheets/site/2.0/12-group-meta.css).

* [Rules](#rules)
* [XHTML diagram](#xhtml-diagram)

<h3 id="rules">Rules</h3>

Meta is one of our simplest design patterns and has few rules.

* Meta is always a definition list (`<dl>`)
* Meta is always wrapped in `<div class="wrapper">`

The child `<dd>` elements may contain anything, but they normally contain dates and times, lists of tags, lists of mods or owners or other associations like Part X of Series Y, and a stats block (which *always* comes at the end!).

<h3 id="xhtml-diagram">XHTML diagram</h3>

The work header is the most familiar example of the meta pattern.

<div class="diagram">
  <ol>
    <li>&lt;div class="wrapper"&gt;
      <ol>
        <li>&lt;dl class="work meta group"&gt;
          <ol>
            <li>&lt;dt class="rating tags"&gt;</li>
            <li>&lt;dd class="rating tags"&gt;</li>
            <li>&lt;dt class="warning tags"&gt;</li>
            <li>&lt;dd class="warning tags"&gt;</li>
            <li>...</li>
            <li>&lt;dt class="stats"&gt;</li>
            <li>&lt;dd class="stats"&gt;
              <ol>
                <li>&lt;dl class="stats"&gt;
                  <ol>
                    <li>...</li>
                  </ol>
                </li>
              </ol>
            </li>
          </ol>
        </li>
      </ol>
    </li>
  </ol>
</div>
