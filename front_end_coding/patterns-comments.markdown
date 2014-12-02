---
layout: front_end_guide
title: Comments Pattern
---
Comments group together information about the commenter, information about the item the comment refers to, the comment itself, and actions pertaining to the comment.

The comment style is declared in [15-group-comments.css](https://github.com/otwcode/otwarchive/blob/master/public/stylesheets/site/2.0/15-group-comments.css).

* [Rules](#rules)
* [Quick reference](#quick-reference)
* [XHTML diagram](#xhtml-diagram)

<h3 id="rules">Rules</h3>

An individual comment is always a `li` contained within an `ol`. These comment lists, or threads, may be nested. Comments are given the class `even` or `odd`.

<h3 id="quick-reference">Quick reference</h3>

<dl class="key"><dt>[...]</dt><dd>always included</dd>
<dt>{...}</dt><dd>sometimes included</dd></dl>

<pre>
[ol thread]
  [li odd comment group]
    []
  [/li]
	{title heading} {byline heading}
	[block module]
	  [heading] {span actions} [/heading]
	  [blockquote userstuff]
	  {p note} {ul actions}
	[block module]
[/ol]
</pre>

<h3 id="xhtml-diagram">XHTML diagram</h3>

This diagram is taken from a challenge profile.

<div class="diagram">
  <ol>
    <li><code>&lt;ol class="thread"&gt;</code>
      <ol>
        <li><code>&lt;li class="odd comment group"&gt;</code>
          <ol>
            <li><code>&lt;h4 class="byline heading"&gt;</code></li>
            <li><code>&lt;div class="icon"&gt;</code></li>
            <li><code>&lt;blockquote class="userstuff"&gt;</code></li>
            <li><code>&lt;h5 class="landmark heading"&gt;</code></li>
            <li><code>&lt;ul class="actions"&gt;</code></li>
          </ol>
        </li>
        <li><code>&lt;li class="even comment group"&gt;</code>
          <ol>
            <li><code>&lt;h3 class="landmark heading"&gt;</code></li>
            <li><code>&lt;ul class="actions"&gt;</code></li>
            <li><code>&lt;h3 class="heading"&gt;</code></li>
            <li><code>&lt;blockquote class="userstuff"&gt;</code></li>
          </ol>        
        </li>
        <li><code>&lt;li&gt;</code>
          <ol>
            <li><code>&lt;ol class="thread"&gt;</code></li>
              <ol>
                <li><code>&lt;li class="even comment group"&gt;</code></li>
                <li><code>&lt;li class="odd comment group"&gt;</code></li>
                <li><code>&lt;li&gt;</code>
                  <ol>
                    <li><code>&li;ol class="thread"&gt;</code>
                      <ol>
                        <li><code>&lt;li class="even comment group"&gt;</code></li>
                      </ol>
                    </li>
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