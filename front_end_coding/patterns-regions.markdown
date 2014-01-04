---
layout: front_end_guide
title: Diagrams of HTML Structures
---
<ol class="diagram">
  <li><code>&lt;body&gt;</code>
  <ol><li><code>&lt;div id="outer" class="wrapper"&gt;</code>
  <ol><li><code>&lt;ul id="skiplinks"&gt;</code></li><code><li>&lt;div id="header" class="region"&gt;</code></li><li><code>&lt;div id="inner" class="wrapper"&gt;</code><ol><li><code>&lt;div id="dashboard" class="region"&gt;</code></li><li><code>&lt;div id="main" class="dashboard region"&gt;</code></li></ol></li><li><code>&lt;div id="footer" class="region"&gt;</code></li></ol></li></ol></li>
</ol>

#### Header

The header is the first region, styled in [ 13-group-blurb.css](https://github.com/otwcode/otwarchive/blob/master/public/stylesheets/site/2.0/03-region-header.css). It contains our branding, the main navigation, and depending on whether or not you are logged in, the log in block or the user navigation.

<ol class="diagram"><li><code>&lt;div id="header" class="region"&gt;</code><ol><li><code>&lt;h1 class="heading"&gt;</code><ol><li><code>&lt;a&gt;</code><ol><li><code>&lt;span&gt;</code></li><li><code>&lt;sup&gt;</code></li><li><code>&lt;img&gt;</code></li></ol></li></ol></li><li>log in block or user navigation</li><li><code>&lt;h3 class="landmark heading"&gt;</code></li><li><code>&lt;ul class="primary navigation actions"&gt;</code><ol><li><code>&lt;li class="dropdown"&gt;</code><ol><li><code>&lt;a class="dropdown-toggle"&gt;</code></li><li><code>&lt;ul class="menu dropdown-menu"&gt;</code><ol><li><code>&lt;li&gt;</code><ol><li><code>&lt;a&gt;</code></li></ol></li><li><code>&lt;li&gt;</code><ol><li><code>&lt;a&gt;</code></li></ol></li><li>...</li></ol></li></ol></li><li><code>&lt;li class="search"&gt;</code><ol><li><code>&lt;form id="search" class="search"&gt;</code><ol><li><code>&lt;fieldset&gt;</code><ol><li><code>&lt;legend&gt;</code></li><li><code>&lt;p&gt;</code><ol><li><code>&lt;label class="landmark"&gt;</code></li><li><code>&lt;input id="site_search" class="text" type="text"&gt;</code></li><li><code>&lt;span class="tip"&gt;</code></li><li><code>&lt;span class="submit actions"&gt;</code><ol><li><code>&lt;input class="button" type="submit"&gt;</code></li></ol></li></ol></li></ol></li></ol></li></ol></li></ol></li><li><code>&lt;div class="clear"&gt;</code></li></ol></li></ol>

##### Log in block

##### User navigation


#### Dashboard

#### Main

#### Footer