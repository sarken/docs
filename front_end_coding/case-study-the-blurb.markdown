---
layout: front_end_guide
title: Case Study - The Blurb
---
On the Archive, we use the term "blurb" to refer to the small summary box which provides a description of a work, a bookmark, a collection, user, or series. Blurbs appear on what we call index pages —- for example, the [works page for the Alternate Universe tag](http://archiveofourown.org/tags/Alternate%20Universe/works) or the [bookmarks page for the user testy](http://archiveofourown.org/users/testy/bookmarks).

![work blurb in the default Archive style](images/workblurb.png)

### Blurb HTML Structure

The work blurb is the most used chunk of HTML code in the Archive, so we've revised it a lot. It has to contain lots of information and allow different ways of accessing its material. The blurb is flexible, accessible, and has multiple redundancies (says the same thing in different ways).

Since we usually have many blurbs listed together, the index page that holds the blurbs is coded as an HTML list, and each blurb is coded as a list item. The XHTML structure, including the outer elements, is laid out like so:

```
<h3 class="landmark heading">Listing Works</h3>
<ol class="work index group">
  <li class="work blurb group" id="work_1234" role="article">
    <!--title, author, fandom-->
    <div class="header module">

      <h4 class="heading" title="title">
        <a href="...">Work Title</a> by <a href="..." class="login author" rel="author">pseud (username)</a>  
      </h4>

      <h5 class="fandoms heading" title="fandom">
        <a href="..." class="tag">Fandom Tags</a>
  	  </h5>

      <!--required tags-->
  	  <ul class="required-tags">
        <li>
          <a href="..." aria-controls="#modal" class="help symbol question modal" title="Symbols key">
            <span class="rating" title="Rating Name">
              <span class="text">Rating Name</span>
            </span>
          </a>
        </li>
        <li> 
          <a href="..." aria-controls="#modal" class="help symbol question modal" title="Symbols key">
            <span class="warnings" title="Warning Names">
              <span class="text">Warning Names</span>
            </span>
          </a>
        </li>
        <li>
          <a href="..." aria-controls="#modal" class="help symbol question modal" title="Symbols key">
            <span class="category" title="Category Names"><span class="text">Category Names</span></span></a>
        </li>
        <li>
          <a href="..." aria-controls="#modal" class="help symbol question modal" title="Symbols key">
            <span class="iswip" title="Work Status">
              <span class="text">Work Status</span>
            </span>
          </a>
        </li>
      </ul>
  	  
  	  <p class="datetime">30 Sep 2013</p>
    </div>
	  
    <!--warnings again, cast, freeform tags-->
    <h6 class="landmark heading">Tags</h6>
    <ul class="tags commas">
  	  <li class='warnings'>
  	    <strong>
  	      <a href="..." class="tag">Warning Tag</a>
  	    </strong>
  	  </li>
  	  <li class='relationships'>
  	    <a href="..." class="tag">Relationship Tag</a>
  	  </li> 
  	  <li class='characters'>
  	    <a href="..." class="tag">Character Tag</a>
  	  </li>
  	  <li class='freeforms'>
  	    <a href="..." class="tag">Additional Tag</a>
  	  </li>
    </ul>

    <!--summary-->	
  	<h6 class="landmark heading">Summary</h6>
  	<blockquote class="userstuff summary" title="summary">
  		<p>This is the summary.</p>
  	</blockquote>
  	
  	<h6 class="landmark heading">Series</h6>
  	<ul class="series">
  	  <li>Part <strong>2</strong> of <a href="...">Series Title</a></li>
  	</ul>

    <!--stats-->
    <dl class="stats" title="stats">
  	  <dt>Words:</dt>
  	  <dd>#</dd>
  	  <dt>Chapters:</dt>
  	  <dd>#/#</dd>
      <dt>Hits:</dt>
      <dd>#</dd>
    </dl>

  </li>
</ol>
```

Here are some of the important things to understand about this layout:

* **The content is presented in *logically readable order**, which has *nothing* to do with the order in which that information is displayed visually in a browser. The title comes first even though visually the first thing you see is the square of the required-tags icons.
* **We don't use inline styles.**  You don't see any CSS embedded into the code like this: `<p style="color: blue;">`. This kind of styling is much harder to track down later on for debugging and maintenance. Please don't do it!
* **We almost always name elements with classes rather than IDs.** Any single ID can only be used once per page. Additionally, CSS rules attached to IDs have higher priority than CSS rules attached to classes, so to make it as easy as possible to create skins, it's better if we use classes by default.
* The class names are space-separated groups of short, common words that describe and document what the information contained in that HTML element is.
* **Classes are nested.** That is, CSS rules from the classes on an outer HTML tag will be inherited by an inner tag, as long as they aren't overridden.
* **A class is only declared on the outermost element that needs it.** That is, we have `work blurb` and then the class `blurb` is inherited all the way down; we don't *also* declare, for instance, `<p class="blurb datetime">`. We just declare `<p class="datetime">` and let it inherit the blurb class from above.
* **We use headings with the `landmark` class and the `title` attribute to label otherwise unlabeled sections of HTML.** These are not displayed with the default CSS rules but are available to screenreaders and other special browsers to help with navigation.

The structure of blurbs should be changed only with extreme caution! Everything about the display can be reorganized (and in fact the blurb can be skinned pretty easily by our users), but the HTML should not be altered.

#### Reasons for the Structure

This structure means it is easy for a piece of software to accurately count the number of items (blurbs) shown in an index. Each new item —- work, index, page region -- is announced by a heading, so users know what information is attached to what title. As a result, a list of headings summarizes the entire index page.

For example, a screenreader user may:

1.  enter search query <kbd>tag: bab5 het long</kbd>
2.  jump to the <kbd>Work List</kbd> landmark heading
3.  hear <samp>"list of 17 items"</samp>
4.  hear <samp>heading level 4 "fic title"</samp>
5.  list headings level 4
6.  jump to item 4 and select title link

This markup, which counts, groups, and names data, allows both linear and non-linear interactions. This means the page makes sense if you read it top to bottom, makes sense if you read parts of it out of context, and helps you jump around. Without this way of writing pages, it's hard to give alternative access technologies the kind of spatial interaction that a visual, mousing browser affords.

### The Blurb Display

As noted above, while the HTML structure of the blurb is incredibly important and should not be altered unless the actual content and purpose of the blurb changes, the display, which is governed entirely by CSS, is much more flexible.

Here you see two different examples of the work blurb from the AO3, one using the default CSS and one using a skin, which have some of their fields mapped to the blurb diagram to help give you the idea.