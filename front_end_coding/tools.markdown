---
layout: front_end_guide
title: Tools
---
Here's the set of basic tools that we'll be using. Please install all of these, even if you have similar tools that you already like -- it will make life easier if we are all using the same set of tools.

### Firefox

In general, the way we will work on projects is to first get them working and looking good in [Firefox](http://www.mozilla.com/en-US/firefox), and then move to cross-browser compatibility towards release time, since this almost invariably involves putting in all sorts of kludginess. 

### Web Developer Toolbar
        
One of the most valuable tools you can have for working on HTML/CSS is a browser plugin that lets you examine and edit the CSS of any web page "live" -- that is, rather than having to edit source code, save a file, and refresh the page every time you want to test some new change to CSS, you can just edit the CSS within your browser until you have it looking the way you want.
        
We recommend the [Web Developer Toolbar](http://chrispederick.com/work/web-developer/), which runs in Firefox or Chrome on any operating system. 

Once you have installed the toolbar, you will be able to edit the CSS of any page you are on with the Edit CSS option:
          
          <img src="images/web_developer_toolbar-edit.png" alt="The Edit CSS menu option highlighted" />
        
This will open a window where you can edit any of the archive stylesheets live and see the results immediately:
          
          <img src="images/web_developer_toolbar-open.png" alt="The Edit CSS window opened" />

If you're working on Internet Explorer compatibility, the [IE Developer Toolbar](http://www.microsoft.com/download/en/details.aspx?id=18359) may be similarly useful.
        
### Firebug or Firebug Lite
        
[Firebug](http://getfirebug.com) is another browser extension that's a great tool for anyone working with JavaScript, HTML and CSS. It lets you edit, debug, and monitor CSS, HTML, and JavaScript live in any web page, in addition to being able to monitor network use, download sizes, and JavaScript efficiency.

Firebug is a Firefox-only extension, but [Firebug Lite](http://getfirebug.com/firebuglite) is compatible with all major browsers, including Internet Explorer 6.
