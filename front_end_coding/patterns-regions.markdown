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

The header is the first region, styled in [ 13-group-blurb.css](https://github.com/otwcode/otwarchive/blob/master/public/stylesheets/site/2.0/03-region-header.css). It contains our branding, the main navigation, and depending on whether or not you are logged in, the log in or greeting block.

<ol class="diagram"><li><code>&lt;div id="header" class="region"&gt;</code><ol><li><code>&lt;h1 class="heading"&gt;</code><ol><li><code>&lt;a&gt;</code><ol><li><code>&lt;span&gt;</code></li><li><code>&lt;sup&gt;</code></li><li><code>&lt;img&gt;</code></li></ol></li></ol></li><li>log in or greeting block</li><li><code>&lt;h3 class="landmark heading"&gt;</code></li><li><code>&lt;ul class="primary navigation actions"&gt;</code><ol><li><code>&lt;li class="dropdown"&gt;</code><ol><li><code>&lt;a class="dropdown-toggle"&gt;</code></li><li><code>&lt;ul class="menu dropdown-menu"&gt;</code><ol><li><code>&lt;li&gt;</code><ol><li><code>&lt;a&gt;</code></li></ol></li><li><code>&lt;li&gt;</code><ol><li><code>&lt;a&gt;</code></li></ol></li><li>...</li></ol></li></ol></li><li><code>&lt;li class="search"&gt;</code><ol><li><code>&lt;form id="search" class="search"&gt;</code><ol><li><code>&lt;fieldset&gt;</code><ol><li><code>&lt;legend&gt;</code></li><li><code>&lt;p&gt;</code><ol><li><code>&lt;label class="landmark"&gt;</code></li><li><code>&lt;input id="site_search" class="text" type="text"&gt;</code></li><li><code>&lt;span class="tip"&gt;</code></li><li><code>&lt;span class="submit actions"&gt;</code><ol><li><code>&lt;input class="button" type="submit"&gt;</code></li></ol></li></ol></li></ol></li></ol></li></ol></li></ol></li><li><code>&lt;div class="clear"&gt;</code></li></ol></li></ol>

##### Log in block

The log in block consists of a link that summons the small log in form when the user has JavaScript enabled or that takes the user to the log in page when they have JavaScript disabled.

<ol class="diagram"><li><code>&lt;div id="login" class="dropdown"&gt;</code><ol><li><code>&lt;p class="user actions"&gt;</code><ol><li><code>&lt;a class="dropdown-toggle"&gt;</code></li></ol></li><li><code>&lt;div id="small_login" class="simple login"&gt;</code><ol><li><code>&lt;form id="new_user_session"&gt;</code><ol><li><code>&lt;dl&gt;</code><ol><li><code>&lt;dt&gt;</code><ol><li><code>&lt;label&gt;</code></li></ol></li><li><code>&lt;dd&gt;</code><ol><li><code>&lt;input class="text" type="text"&gt;</code></li></ol></li><li><code>&lt;dt&gt;</code><ol><li><code>&lt;label&gt;</code></li></ol></li><li><code>&lt;dd&gt;</code><ol><li><code>&lt;input class="text" type="text"&gt;</code></li></ol></li></ol></li><li><code>&lt;p class="submit actions"&gt;</code><ol><li><code>&lt;label class="action"&gt;</code><ol><li><code>&lt;input type="checkbox"&gt;</code></li></ol></li><li><code>&lt;input type="submit"&gt;</code></li></ol></li><li><code>&lt;ul class="footnote actions"&gt;</code><ol><li><code>&lt;li&gt;</code><ol><li><code>&lt;a&gt;</code></li></ol></li><li><code>&lt;li&gt;</code><ol><li><code>&lt;a&gt;</code></li></ol></li></ol></li></ol></li></ol></li></ol></li></ol>

##### Greeting block

The greeting block contains the user's icon and navigation items that are only available to logged in users.

<ol class="diagram"><li><code>&lt;div id="greeting"&gt;</code><ol><li><code>&lt;h3 class="landmark heading"&gt;</code></li><li><code>&lt;ul class="user navigation actions"&gt;</code><ol><li><code>&lt;li class="dropdown"&gt;</code><ol><li><code>&lt;a class="dropdown-toggle"&gt;</code></li><li><code>&lt;ul class="menu dropdown-menu"&gt;</code><ol><li><code>&lt;li&gt;</code><ol><li><code>&lt;a&gt;</code></li></ol></li></ol></li></ol></li><li><code>&lt;li class="dropdown"&gt;</code><ol><li><code>&lt;a class="dropdown-toggle"&gt;</code></li><li><code>&lt;ul class="menu dropdown-menu"&gt;</code><ol><li><code>&lt;li&gt;</code><ol><li><code>&lt;a&gt;</code></li></ol></li><li><code>&lt;li&gt;</code><ol><li><code>&lt;a&gt;</code></li></ol></li></ol></li></ol></li><li><code>&lt;li&gt;</code><ol><li><code>&lt;a&gt;</code></li></ol></li></ol></li><li><code>&lt;p class="icon"&gt;</code><ol><li><code>&lt;a&gt;</code><ol><li><code>&lt;img class="icon"&gt;</code></li></ol></li></ol></li></ol></li></ol>

#### Dashboard

<ol class="diagram"><li><code>&lt;div id="dashboard" class="region"&gt;</code><ol><li><code>&lt;h4 class="landmark heading"&gt;</code></li><li><code>&lt;ul class="navigation actions"&gt;</code><ol><li><code>&lt;li&gt;</code><ol><li><code>&lt;a&gt;</code></li></ol></li><li><code>&lt;li&gt;</code><ol><li><code>&lt;a&gt;</code></li></ol></li><li><code>&lt;li&gt;</code><ol><li><code>&lt;span class="current"&gt;</code></li></ol></li></ol></li><li><code>&lt;h4 class="landmark heading"&gt;</code></li><li><code>&lt;ul class="navigation actions"&gt;</code></li></ol></li></ol>

#### Main

#### Footer