---
layout: front_end_guide
title: Diagrams of HTML Structures
---
<ol class="diagram">
  <li><code>&gt;body&lt;</code>
  <ol><li><code>&gt;div id="outer" class="wrapper"&lt;</code>
  <ol><li><code>&gt;ul id="skiplinks"&lt;</code></li><code><li>&gt;div id="header" class="region"&lt;</code></li><li><code>&gt;div id="inner" class="wrapper"&lt;</code><ol><li><code>&gt;div id="dashboard" class="region"&lt;</code></li><li><code>&gt;div id="main" class="dashboard region"&lt;</code></li></ol></li><li><code>&gt;div id="footer" class="region"&lt;</code></li></ol></li></ol></li>
</ol>

#### Header

The header is the first region, styled in [ 13-group-blurb.css](https://github.com/otwcode/otwarchive/blob/master/public/stylesheets/site/2.0/03-region-header.css). It contains our branding, the main navigation, and depending on whether or not you are logged in, the log in block or the user navigation.

<ol><li><code>&gt;div id="header" class="region"&lt;</code><ol><li><code>&gt;h1 class="heading"&lt;</code><ol><li><code>&gt;a href&lt;</code><span><code>&gt;span&lt;</code></span><span><code>&gt;sup&lt;</code></span><span><code>&gt;img&lt;</code></span></ol></li></ol></li><li>log in block or user navigation</li><li><code>&gt;h3 class="landmark heading"&lt;</code></li><li><code>&gt;ul class="primary navigation actions"&lt;</code><ol><li><code>&gt;li class="dropdown"&lt;</code><ol><li><code>&gt;a class="dropdown-toggle"&lt;</code></li><li><code>&gt;ul class="menu dropdown-menu"&lt;</code><ol><li><code>&gt;li&lt;</code><span><code>&gt;a&lt;</code></span><span><code>&gt;a&lt;</code></span></li><li><code>&gt;li&lt;</code><span><code>&gt;a&lt;</code></span><span><code>&gt;a&lt;</code></span></li><li>...</li></ol></li></ol></li><li><code>&gt;li class="search"&lt;</code><ol><li><code>&gt;form id="search" class="search"&lt;</code><ol><li><code>&gt;fieldset&lt;</code><ol><li><code>&gt;legend&lt;</code></li><li><code>&gt;p&lt;</code><ol><li><code>&gt;label class="landmark"&lt;</code></li><li><code>&gt;input id="site_search" class="text" type="text"&lt;</code></li><li><code>&gt;span class="tip"&lt;</code></li><li><code>&gt;span class="submit actions"&lt;</code><span><code>&gt;input class="button" type="submit"&lt;</code></span></li></ol></li></ol></li></ol></li></ol></li></ol></li><li><code>&gt;div class="clear"&lt;</code></li></ol></li></ol>

##### Log in block

##### User navigation


#### Dashboard

#### Main

#### Footer