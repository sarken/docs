---
layout: front_end_guide
title: Writing a Skin
---
Anyone with an Archive account can customize the way the Archive is presented to them by creating and applying a site skin that either modifies the default display or restyles the Archive from scratch. 

The skin system is also a great way to get familiar with CSS in general or the Archive's class structure. You can create a new skin by logging in and going to [the Skins index](http://archiveofourown.org/skins), where you will find a Create Skin button. Click that and you will be taken to a form, which will already be set up to create a Site Skin -- you just need to enter a title.

### Styling the Header, Dashboard, Main, and Footer Regions

Here we'll walk through a simple skin that modifies the Archive's default appearance by changing fonts and colors, adding images, and adjusting margins and borders.

1.  Let's change the font and the font color for the entire page using the universal selector (`*`) and `!important`, which will ensure that our changes override the defaults across the whole site.

  ```css
  * {
    font-family: Verdana, Tahoma, Helvetica, Arial, sans-serif !important;
    color: #444;
  }
  ```

  *Note*: Once you've entered the style block into the CSS field, you'll need to select "Submit" after the form and "Use" on the following page to see the changes. After that, changes will be visible immediately after using the "Update" button on the skin form.

2.  Now let's use an image for the background of the page. Background images tile in all directions by default.

  We'll use a cheerful stripe pattern called [sing together](http://www.colourlovers.com/pattern/850926/sing_together) by [electroCUTE!](http://www.colourlovers.com/lover/electroCUTE%21), which we've uploaded to [tinypic](http://tinypic.com). (For your own private skins you can host your images anywhere; [Photobucket](http://photobucket.com) and [Image Shack](http://imageshack.us) are common alternatives. Because you are the only one seeing your skin, you probably don't need to worry about running out of bandwidth.) 

  We'll also set the lightest color from the corresponding [like fireflies](http://www.colourlovers.com/palette/1172215/like_fireflies) palette as the fallback color to make sure we don't see the usual white even if our image fails to load.

  ```css
  body {
    background: #F6F6C6 url(http://i47.tinypic.com/2mfc7ev.png);
  }
  ```

3.  The Archive's signature red clashes with that, so let's take the pinkish red from the palette and use that to replace the red in the header and footer. We'll also change the borders on the header and footer and remove the 3D effect from the header.

  ```css
  #header ul.primary, #footer {
    background: #FE8665;
  }
  
  #header ul.primary {
    border-bottom: 5px #FCDF7D solid;
    box-shadow: none;
  }
  
  #footer {
    border-top: 5px #FCDF7D solid;
  }
  ```

4.  It's hard to read on that busy pattern, so let's give the main content of the site a translucent white background. We'll let the pattern stick out on the sides by setting some margins, and we'll also round off the corners and give our white area a light shadow. We've previously been using hexadecimal values for the colors, but here we'll switch to RGBa to lower the opacity of our colors. (If you're using Internet Explorer 8 or earlier, you'll see solid colors instead. If this were the official Archive layout, we might use a special stylesheet to add transparency for Internet Explorer 8 and lower.)

  ```css
  #main {
    background: rgba(255,255,255,0.9);
    margin: 1em;
    border-radius: 1em;
    box-shadow: 1px 1px 2px rgba(0,0,0,0.25);
  }
```

5.  Pages that belong to users or collections have an additional navigation section called the dashboard. Not only does that need to be styled, but we also need to adjust `#main` slightly so it still has margins when the dashboard is present. We'll give the dashboard a translucent yellow background, rounded edges, no borders, and highlighting for current and hover areas.

  ```css
  #main.dashboard {
    margin-right: 1em;
  }
  
  #dashboard.own {
    border: none;
  }
  
  #dashboard ul {
    background: rgba(252,223,125,0.9);
    border-top: none;
    text-align: center;
    margin-top: 2px;
    border-radius: 1em;
  }

  #dashboard .current, #dashboard a:hover {
    background: rgba(255,255,255,0.35);
  }
  ```

### Styling Works

All user copy is placed inside either `<blockquote class="userstuff">` or `<div class="userstuff">`, so you can style it by targeting `.userstuff` as a whole or by using `.userstuff` along with another selector. 

Let's add the following to our site skin to make a drastic change to all user copy:

```css
.userstuff { 
  background: #F6F6C6; 
  border: 1px #FCDF7D solid; 
  border-radius: 1em;
}
``` 

If you spend a few minutes browsing the site with that skin, you'll notice that works aren't the only user copy on the site. Profiles, collection pages, work and bookmark blurbs, and administrative pages (e.g. the FAQ) all contain user copy and are also affected by that style.

If you *only* want to change the way works are displayed, using `#workskin` is your best bet. It's primary function is to help work creators make work skins, which style the work for anyone who views it on the Archive, but it is also an effective way to modify works for your personal site skin. 

You may want to...

* Change the font: `#workskin { font-family: Georgia, serif; }`
* Indent paragraphs: `#workskin p { text-indent: 2.5em; }`
* Hide the work notes: `#workskin .preface .notes { display: none; }`

(You can go back and delete the `.userstuff` styles now -- we won't be using it elsewhere in the tutorial.)

#### Work Metadata

The work view has a lot of metadata on it, but other pages such as user stats, user profiles, and series pages also contain metadata that you might now want to style. The metadata is *not* inside `#workskin`, but you can use `.work-show .meta` to target the metadata for works.

You might want to suppress some metadata: 

* Hide the whole meta block: `.work-show .meta { display: none; }`
* ...or just the bits you don't want to know: `.work-show .meta .warning, .work-show .meta .stats { display: none; }`

Or you might want to highlight some metadata:

* Highlight the rating with pink: `.work-show .meta .rating { background: #FE8665; }`
* Make the fandoms bold: `.work-show .meta .fandoms { font-weight: bold; }`
