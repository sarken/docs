---
layout: front_end_guide
title: Classes
---
Classes are used to add structural meaning. A good class describes more specifically the function of the element to which it is applied. A bad class is something like `red` ; a good class is something like `warning`. (Imagine that you were creating a skin for people with red-green color blindness, and you wanted to change the appearance of words using the class `red` to be the color blue! That would be very confusing and therefore harder to maintain.)

* [Rules](#rules)
* ["What kind and where?"](#what-kind-and-where)
* [Rails classes](#rails-classes)

<h3 id="rules">Rules</h3>

* Classes are general and written in English (U.S). Ideally, they are short words in common usage.
* Do **not** give every element on every page a unique class. Classes are inherited from their parent element and can be combined together to style elements uniquely.
* Do **not** give elements very specific names.

If you find yourself combining several words to make a class, like `english_user_information`, stop and think whether you could use several more general classes: `english user information`.

You should only write the class on the highest element it applies to on each level. All the elements nested inside this parent will inherit its properties anyway, and otherwise you could end up double-applying the attributes of that class to the nested elements.

Our classes are how we describe and document our data, so it's very important to use them consistently and accurately. If you find a class that doesn't fit this system, it's probably a mistake and needs fixing. The main exceptions are classes for jQuery plugins, since it is easier to keep plugins up to date if we *don't* modify the class names. However, if you're writing new jQuery for the Archive, please keep our naming system in mind.

<h3 id="what-kind-and-where">"What kind and where?"</h3>

It might be useful to look at some [diagrams of pages](patterns) on our Archive to really understand that in CSS, we write a path *to* places in our XHTML; we don't need to give everything a unique name, because we describe it: "what kind and where".

For example, we use a dotted line to underline all tag links: `a.tag { border-bottom: 1px dotted; }`. If we want to change how tag links look on bookmark blurbs, we don't add a new `bookmark-tag` class in the HTML -- we just use the bookmark tags' unique path in the DOM: `.bookmark a.tag { border-bottom: none; }`

<h3 id="rails-classes">Rails classes</h3>

Rails automatically generates a unique class on `<div id="main">` on each page, named by the view partial that `div` calls. This means that each page on the Archive can have rules set independently, which is very useful for tweaking the layout, but should not be used as a core technique.

* The [Media Index](http://archiveofourown.org/media) has the Rails class `media-index`.

* The [works index for testy](http://archiveofourown.org/users/testy/works) has the Rails class `works-index`, and we also tell it to automatically add `dashboard` and `filtered` to the page because it contains dashboard navigation and filters.