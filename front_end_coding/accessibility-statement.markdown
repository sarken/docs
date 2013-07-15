---
layout: front_end_guide
title: Accessibility Statement
---
### Everyone is Welcome

This page is an overview of ways we have tried to make the Archive accessible. Accessibility is always a work in progress, so this document will and should change.

If you have any questions or comments, please do send us [feedback](http://archiveofourown.org/support). Portions of this document have been taken from [diveintoaccessibility.com](http://diveintoaccessibility.com). 

#### Standards Compliance

Note: many people have access to the AO3 code and can edit it, so standards compliance is generally a moving target for us. However, this represents the standards we strive to meet; where we sometimes miss the mark, we will aim to get back into compliance with code review at a future date.

When we talk about pages complying with a standard, we mean that the *site framework* (that is, the code for the archive interface surrounding user content like fanworks, summaries, descriptions, etc) complies. We do not try to validate our user-generated content, though we do parse it for display using [Nokogiri](http://nokogiri.org), an XHTML-compliant parser. But as a rule, we aim to encourage valid and accessible coding from our users through advocacy and training, not auto formatting. 

1.  Most importantly, all pages on this site use structured semantic markup. `h1` is used for the site name. `h2` is used for the individual page name. `h3` is used for section headings within the page. `h4` is used for article names, like the name of commenter or the titles on a list of works. For example, on this page, JAWS users can skip to the next section within the accessibility statement by pressing <kbd>ALT+INSERT+3</kbd>.

2. All framework pages on this site are or work towards <acronym title="Web Content Accessibility Guidelines">WCAG</acronym> <acronym title="triple A">AAA</acronym> approved, complying with all [priority 1, 2, and 3 guidelines](http://www.w3.org/TR/WAI-WEBCONTENT/full-checklist.html) of the [World Wide Web Consortium Web Content Accessibility Guidelines](http://www.w3.org/TR/WCAG10/). This is a judgement call. 

4.  All framework pages on this site are <a href="http://www.cynthiasays.com/">Section 508 approved</a>, complying with all of the <acronym title="United States">U.S.</acronym> Federal Government <a href="http://www.section508.gov/">Section 508 Guidelines</a>.  Again, a judgement call.  

5.  While ARIA roles cannot be validated with an XHTML 1.0 Strict checker, all framework pages on this site otherwise <a href="http://validator.w3.org/">validate as <acronym title="extensible hypertext markup language">XHTML</acronym> 1.0 Strict</a>.  This is not a judgement call; a program can determine with 100% accuracy whether a page is valid XHTML. For example, you can enter your AO3 user page URL on the [W3 validator](http://validator.w3.org/check) and check it for XHTML validity.

### Languages

The Archive is an international development, made by people who speak lots of different languages. Our goal is to build a translation tool to allow the archive interface to be translated into any language that has volunteers to work on it.

### Navigation Aids

1.  [BREADCRUMBS]

2.  We aim to make our help and FAQs accessible in multiple ways. 

3.  We have tried to provide help that is not biased towards sighted or mouse methods of using archive, by describing pages and interactions in several different ways, but we know we could always use help at doing this better, so please do [send us feedback](http://archiveofourown.org/support).

4.  Our help buttons are styled text, so you can make them bigger if they're hard to see.

5.  The home page and all archive pages include a search box. Advanced search options are available from any search results page and from the search menu.

6.  All navigation, sorting, actions, and page regions are announced by a relevant and descriptive heading. These headings are hidden from visual browsers by default, but we have a skin you can use to show these headings to any browser.

7.  Blocks containing unlabelled content have been given titles, so you don't have to work out what something is from its context.

### Links

1.  Some links have title attributes which describe the link in greater detail, unless the text of the link already fully describes the target (such as the headline of an article).

2.  Links are written to make sense out of context.

3.  Navigation and action links are visually styled as large and distinct buttons. They can be scaled up with text zoom to make them easier to click on with a mouse or a joystick. We're working on a 'bright button' and 'big button' skin to make them easier to see and click, and a 'fixed button' skin so they're always on the screen, which might be more useful if you're using a switch interface.

### Forms

1.  Our forms are laid out in a limited and regular number of ways, and we've tried to make it clear when a form begins and ends.

2.  We have labelled everything to make it clear what we're asking you to do. In very short forms those labels are hidden but we're working on a skin you can use to show them.

3.  We've written our forms so that you can click on the text to check the little box or button.

### Images

1. All images used in this site are described with text alternatives. Purely decorative graphics include null `alt` attributes.


2. Our logo has a spoken or text equivalent, which communicates the *intent and feel* of the graphic.

### Visual Design

1.  The Archive uses cascading style sheets for visual layout.

2.  The Archive uses only relative font sizes, compatible with the user-specified "text size" option in visual browsers. 

3.  If your browser or browsing device does not support stylesheets at all, the content of each page is still readable.

### Alternative Visual Layouts (Skins)

You can skin the archive interface for yourself in any way that you find useful. We also work on (and welcome user contributions of!) public skins that help solve accessibility issues. 

We try to design in an accessible way, which means that we've made the interface *open* for you to *adapt* easily, rather than thinking to know what you need better than you do yourself. AO3 is lucky in that there are people using, coding, and testing via many different methods. But we are still limited: we design to be open to everything but can only test with the tools available to us, which are, roughly: about thirty browsers for screen and handheld with various customizations, Lynx, Chromevox, Fangs, switchXS, Dragon Dictate, mouseless browsing and Vimium. So if you come across a hurdle, or something that could be better, it's really a big help for you to send it in. 

You don't have to know how to code (though we'll teach you that too if you like) to adapt the Archive. If you contact [Support](http://archiveofourown.org/support) with layout changes that would help you, Support will alert the coding team to your needs, and the coding team can attempt to make the necessary changes to the Archive's default style or to design a skin to address your needs.

### JavaScript

We use JavaScript on the AO3 to improve usability and performance, but all our content and core functionality is accessible with JavaScript turned off.


### Screenreaders

1.  We use headings and lists to structure our pages. You can jump around the page regions by heading. Lists should always give you an accurate count of the number of different items on a page. If they don't, please [tell us](http://archiveofourown.org/support).

2.  We have implemented basic ARIA landmark roles and as we go along we are adding in more WAI-ARIA attributes as we figure out how best to use them.

3.  We have an experimental aural stylesheet. We are investigating supporting a say-instead or pronunication dictionary. If you would like to help, please [volunteer](http://transformativeworks.org/volunteer) or send us [feedback](http://archiveofourown.org/support).

4.  We support aural skins.
				
### Keyboard Access

1.  We write our pages in a logical order, so you can tab through the whole Archive. We decided not to add accesskeys, because we know they can sometimes mess up your own shortcuts.

2.  We are looking at using a new way to develop a really good keyboard interface, but this will take us a long time.

### Small Screens, Slow Internet

We try and keep our site pages relatively small and functioning on screens of any size including mobile devices.
