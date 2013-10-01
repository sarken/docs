---
layout: front_end_guide
title: Case Study The Blurb
---
On the Archive, we use the term "blurb" to refer to the small summary box which provides a description of a work, a bookmark, a collection, user, or series. Blurbs appear on what we call index pages —- for example, the [works page for the Alternate Universe tag](http://archiveofourown.org/tags/Alternate%20Universe/works) or the [bookmarks page for the user testy](http://archiveofourown.org/users/testy/bookmarks).

![work blurb in the default Archive style](/../images/workblurb.png)

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
        <a href="...">Work's Title</a> by <a href="..." class="login author" rel="author">testy</a>  
      </h4>

      <h5 class="fandoms heading" title="fandom">
        <a href="..." class="tag">Work's Fandom</a>
  	  </h5>

      <!--required tags-->
  	  <ul class="required-tags">
        <li>
          <a href="..." aria-controls="#modal" class="help symbol question modal" title="Symbols key">
            <span class="rating-general-audience rating" title="General Audiences">
              <span class="text">General Audiences</span>
            </span>
          </a>
        </li>
        <li> 
          <a href="..." aria-controls="#modal" class="help symbol question modal" title="Symbols key"><span class="warning-no warnings" title="No Archive Warnings Apply"><span class="text">No Archive Warnings Apply</span></span>
          </a>
        </li>
        <li>
          <a href="..." aria-controls="#modal" class="help symbol question modal" title="Symbols key"><span class="category-multi category" title="F/M, M/M"><span class="text">F/M, M/M</span></span></a>
        </li>
        <li>
          <a href="..." aria-controls="#modal" class="help symbol question modal" title="Symbols key"><span class="complete-no iswip" title="Work in Progress"><span class="text">Work in Progress</span></span>
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
  	      <a href="..." class="tag">No Archive Warnings Apply</a>
  	    </strong>
  	  </li>
  	  <li class='relationships'>
  	    <a href="..." class="tag">Female Character/Male Character</a>
  	  </li> 
  	  <li class='relationships'>
  	    <a href="..." class="tag">Male Character/Other Male Character</a>
  	  </li>
  	  <li class='characters'>
  	    <a href="..." class="tag">Female Character - Character</a>
  	  </li>
  	  <li class='characters'>
  	    <a href="..." class="tag">Male Character</a>
  	  </li>
  	  <li class='characters'>
  	    <a href="..." class="tag">Other Male Character</a>
  	  </li>
  	  <li class='freeforms'>
  	    <a href="..." class="tag">Tags are Fun</a>
  	  </li>
  	  <li class='freeforms'>
  	    <a href="..." class="tag">Additional Tag</a>
  	  </li>
    </ul>

    <!--summary-->	
  	<h6 class="landmark heading">Summary</h6>
  	<blockquote class="userstuff summary" title="summary">
  		<p>This is the summary of my work. It quotes my work.</p>
      <blockquote>
        <p>It was a dark and stormy afternoon.</p>
      </blockquote>
  	</blockquote>
  	
  	<h6 class="landmark heading">Series</h6>
  	<ul class="series">
  	  <li>Part <strong>2</strong> of <a href="...">Brand New Series of Regression Testing</a></li>
  	</ul>

    <!--stats-->
    <dl class="stats" title="stats">
  	  <dt>Words:</dt>
  	  <dd>496</dd>
  	  <dt>Chapters:</dt>
  	  <dd>1/?</dd>
      <dt>Hits:</dt>
      <dd>0</dd>
    </dl>

  </li>
</ol>
```

Here are some of the important things to understand about this layout:

* *The content is presented in *logically readable order*, which has **nothing** to do with the order in which that information is displayed visually in a browser. The title comes first even though visually the first thing you see is the square of the required-tags icons.
* *We don't use inline styles.*  You don't see any CSS embedded into the code like this: `<p style="color: blue;">`. This kind of styling is much harder to track down later on for debugging and maintenance. Please don't do it!
* *We almost always use classes rather than IDs.* CSS rules attached to ids have higher priority than CSS rules attached to classes, so to make it as easy as possible to create skins, it's better if we use classes by default.
* The class names are short, common single words. We use them in combination.
* The class names describe and document what the information contained in that HTML element is.
* *Classes are nested.* That is, CSS rules from the classes on an outer HTML tag will be inherited by an inner tag, as long as they aren't overridden.
* A class is only declared on the outermost element that needs it. That is, we have work blurb and then the class blurb is inherited all the way down; we don't ALSO declare, for instance, `<p class="blurb datetime">`. We just declare `<p class="datetime">` and let it inherit the blurb class from above.
* *We use headings with the `landmark` class and the `title` attribute to label otherwise unlabeled sections of HTML.* These are not displayed with the default CSS rules but are available to screenreaders and other special browsers to help with navigation.
