---
layout: front_end_guide
title: Style Guide
---
To establish the Archive's identity and to keep a consistent look and feel across the site, we have a specific set of styles we use. These are closely tied to the styles of our parent organization and our sister projects, so **do not deviate from the styles in this document** without approval from the Design Lead, Front End Lead, or AD&T Committee Chair.

* [General](#general)
    * [Copy](#general-copy)
    * [Logo](#general-logo)
    * [Fonts](#general-fonts)
    * [Colors](#general-colors)
* [Screen](#screen)
    * [Fonts](#screen-fonts)
    * [Colors](#screen-colors)
        * [Variations](#screen-colors-variations)
        * [States](#screen-colors-states)
        * [System and error messages](#screen-colors-system-and-error-messages)
* [Print](#print)
    * [Fonts](#print-fonts)
    * [Colors](#print-colors)

<h3 id="general">General</h3>

There are some guidelines we follow regardless of media.

<h4 id="general-copy">Copy</h4>

When writing copy for the Archive (e.g. help text), use American spelling, a single space between sentences, and a capital "A" when referring to the Archive.

<h4 id="general-logo">Logo</h4>

![Archive logo](images/logo.png)

The red used in our logo is `#990000`, which can be shorthanded as `#900`. Do not change the color. If there is insufficient contrast between the logo and the background, a border may be added.

The logo has an aspect ratio of 117:80. Do not change the aspect ratio.

<h4 id="general-fonts">Fonts</h4>

When the Archive name accompanies the logo or is used as a masthead, it should be written in <span class="georgia serif">Georgia</span>.

<h4 id="general-colors">Colors</h4>

<div>
  <table summary="The five colors we use in our materials, and their hexadecimal, CMYK, and RGB values">
    <caption>We use five basic colors in all our materials</caption>
    <thead>
      <tr>
        <th scope="col" colspan="2">Color</th>
        <th scope="col"><abbr title="hexadecimal">HEX</abbr></th>
        <th scope="col"><abbr title="Cyan">C</abbr></th>
        <th scope="col"><abbr title="Magenta">M</abbr></th>
        <th scope="col"><abbr title="Yellow">Y</abbr></th>
        <th scope="col"><abbr title="Key">K</abbr></th>
        <th scope="col"><abbr title="Red">R</abbr></th>
        <th scope="col"><abbr title="Green">G</abbr></th>
        <th scope="col"><abbr title="Blue">B</abbr></th>
        <td></td>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th scope="row">Red</th>
        <td class="red color">&nbsp;</td>
        <td>#990000</td>
        <td>26</td>
        <td>100</td>
        <td>100</td>
        <td>28</td>
        <td>187</td>
        <td>0</td>
        <td>17</td>
        <td class="red color">&nbsp;</td>
      </tr>
      <tr>
        <th scope="row">White</th>
        <td class="white color">&nbsp;</td>
        <td>#ffffff</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>255</td>
        <td>255</td>
        <td>255</td>
        <td class="white color">&nbsp;</td>
      </tr>
      <tr>
        <th scope="row">Black</th>
        <td class="black color">&nbsp;</td>
        <td>#000000</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>100</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td class="black color">&nbsp;</td>
      </tr>
      <tr>
        <th scope="row">Light gray</th>
        <td class="light-gray-ddd color">&nbsp;</td>
        <td>#dddddd</td>
        <td colspan="4">web only</td>
        <td>221</td>
        <td>221</td>
        <td>221</td>
        <td class="light-gray-ddd color">&nbsp;</td>
      </tr>
      <tr>
        <th scope="row">Dark gray</th>
        <td class="dark-gray-333 color">&nbsp;</td>
        <td>#333333</td>
        <td colspan="4">web only</td>
        <td>51</td>
        <td>51</td>
        <td>51</td>
        <td class="dark-gray-333 color">&nbsp;</td>
      </tr>
    </tbody>
  </table>
</div>

<h3 id="screen">Screen</h3>

Our e-mail styles also follow these screen styles.

<h4 id="screen-fonts">Fonts</h4>

<dl>
<dt>Headings, subheadings, titles, addresses</dt>
<dd>400 weight, <span class="georgia serif">Georgia</span>, <span class="serif">serif</span>
<ul><li>The serif font stack should be used in the structural elements <code>h1</code>, <code>h2</code>, <code>h3</code>, <code>h4</code>, <code>h5</code>, <code>h6</code> or in elements with the class <code>heading</code>.</li>
<li><span class="georgia serif">Georgia</span> is a core web font; this means that everyone has it installed on their computer.</li>
<li>If <span class="georgia serif">Georgia</span> is not available, we fall back to the user's default <span class="serif">serif</span> font.</li></ul></dd>
<dt>Body text</dt>
<dd><span class="lucida-grande sans-serif">Lucida Grande</span>, <span class="lucida-sans sans-serif">Lucida Sans Unicode</span>, <span class="gnu-unifont sans-serif">GNU Unifont</span>, <span class="verdana sans-serif">Verdana</span>, <span class="helvetica sans-serif">Helvetica</span>, <span class="sans-serif">sans-serif</span>
<ul><li>This sans-serif font stack should be used in the main body of the text, on navigation actions, and on almost anything that isn't a heading.</li>
<li><span class="lucida-grande sans-serif">Lucida Grande</span> is an Apple system font that all Mac users have; <span class="lucida-sans sans-serif">Lucida Sans Unicode</span> is the Windows equivalent. <span class="gnu-unifont sans-serif">GNU Unifont</span> is system font on most free operating systems (e.g. Linux).</li>
<li><span class="verdana sans-serif">Verdana</span> is a core web font that nearly everyone has.</li></ul></dd>
<dt>Dates, pre-formatted text, and code</dt>
<dd><span class="monaco monospace">Monaco</span>, <span class="consolas monospace">Consolas</span>, <span class="courier monospace">Courier</span>, <span class="monospace">monospace</span>
<ul><li>We use monospace fonts for <code>kbd</code>, <code>tt</code>, <code>code</code>, <code>var</code>, <code>pre</code> and many instances of dates and times, which typically have the class <code>datetime</code>.</li>
<li><span class="monaco monospace">Monaco</span> is an Apple system font that all Mac users have. <span class="consolas monospace">Consolas</span> is the Windows equivalent.</li>
<li><span class="courier monospace">Courier</span> is a core web font that nearly everyone has.</li></ul></dd>
</dl>

<h4 id="screen-colors">Colors</h4>

<table summary="The colors we use in our website, how they are used, and their hexadecimal and RGB values">
<caption>We use these colors on the screen</caption>
<thead>
<tr>
<th scope="col" colspan="2">Color</th>
<th scope="col">Use</th>
<th scope="col"><abbr title="hexadecimal">HEX</abbr></th>
<th scope="col"><abbr title="Red">R</abbr></th>
<th scope="col"><abbr title="Green">G</abbr></th>
<th scope="col"><abbr title="Blue">B</abbr></th>
<td></td>
</tr>
</thead>
<tbody>
<tr>
<th scope="row">Red</th>
<td class="red color">&nbsp;</td>
<td>Logo, masthead, blurb titles, tag hover</td>
<td>#990000</td>
<td>187</td>
<td>0</td>
<td>17</td>
<td class="red color">&nbsp;</td>
</tr>
<tr>
<th scope="row">White</th>
<td class="white color">&nbsp;</td>
<td>Page background</td>
<td>#ffffff</td>
<td>255</td>
<td>255</td>
<td>255</td>
<td class="white color">&nbsp;</td>
</tr>
<tr>
<th scope="row">Dark gray</th>
<td class="dark-gray-2a2a2a color">&nbsp;</td>
<td>Text</td>
<td>#2a2a2a</td>
<td>42</td>
<td>42</td>
<td>42</td>
<td class="dark-gray-2a2a2a color">&nbsp;</td>
</tr>
<tr>
<th scope="row">Darkest gray</th>
<td class="darkest-gray-111 color">&nbsp;</td>
<td>Links</td>
<td>#111111</td>
<td>17</td>
<td>17</td>
<td>17</td>
<td class="darkest-gray-111 color">&nbsp;</td>
</tr>
</tbody>
</table>

<h5 id="screen-colors-variations">Variations</h5>

We use a range of grays to color boxes, mark borders, and create shadows.

<ul class="swatches">
<li style="background:#eee">#eee</li>
<li style="background:#ddd">#ddd</li>
<li style="background:#ccc">#ccc</li>
<li style="background:#bbb">#bbb</li>
<li style="background:#aaa">#aaa</li>
<li style="background:#999">#999</li>
<li style="background:#777; color:#fff">#777</li>
<li style="background:#666; color:#fff">#666</li>
<li style="background:#555; color:#fff">#555</li>
<li style="background:#444; color:#fff">#444</li>
<li style="background:#333; color:#fff">#333</li>
</ul>

The header, footer, and tag clouds use a few more reds.

<ul class="swatches">
<li style="background:#a00;">#a00</li>
<li style="background:#800; color:#fff">#800</li>
<li style="background:#700; color:#fff">#700</li>
<li style="background:#600; color:#fff">#600</li>
<li style="background:#500; color:#fff">#500</li>
<li style="background:#400; color:#fff">#400</li>
<li style="background:#300; color:#fff">#300</li>
<li style="background:#200; color:#fff">#200</li>
</ul>

<h5 id="screen-colors-states">States</h5>

Some states have their own colors.

<ul class="swatches">
<li style="background:#008000; color: #fff;">#008000 green: replied, offered</li>
<li style="background:#daa520">#876714 gold: offered and requested</li>
</ul>

<h5 id="screen-colors-system-and-error-messages">System and error messages</h5>

System and error messages are color-coded and use their own separate color scheme.

System and flash messages use these colors:

<ul class="messages swatches">
<li style="background:#d1e1ef; border:1px solid #c2d2df">blue: success, messages, additional information. The background is #d1e1ef with a border of #c2d2df. It uses the main text color.</li>
<li style="background:#efd1d1; border: 1px solid #900">red: error, go back and fix this problem. The background is #efd1d1 with a border of #900.</li>
<li style="background:#ffe34e; border: 1px solid #d89e36; color: #000">yellow: warning, click to proceed, correct this error before you proceed. #ffe34e with a border of #d89e36 and #000 text.</li>
</ul>

LiveValidation messages on forms use these colors:

<ul class="messages swatches">
<li style="background:#0c0">#0c0 green: success</li>
<li style="background:#c00">#c000 red: error</li>
</ul>

<h3 id="print">Print</h3>

Our print styles are defined in [27-role-print.css](https://github.com/otwcode/otwarchive/blob/master/public/stylesheets/site/2.0/27-role-print.css).

<h4 id="print-fonts">Fonts</h4>

Rather than using a specific font, all print text uses the <span class="serif">serif</span> font family. This tells the system to use its default serif font.

<h4 id="print-colors">Colors</h4>

<table summary="The two colors we use in our print materials, and their hexadecimal, CMYK, and RGB values">
<caption>We use two colors in our print styles</caption>
<thead>
<tr>
<th scope="col" colspan="2">Color</th>
<th scope="col"><abbr title="hexadecimal">HEX</abbr></th>
<th scope="col"><abbr title="Cyan">C</abbr></th>
<th scope="col"><abbr title="Magenta">M</abbr></th>
<th scope="col"><abbr title="Yellow">Y</abbr></th>
<th scope="col"><abbr title="Key">K</abbr></th>
<th scope="col"><abbr title="Red">R</abbr></th>
<th scope="col"><abbr title="Green">G</abbr></th>
<th scope="col"><abbr title="Blue">B</abbr></th>
<td></td>
</tr>
</thead>
<tbody>
<tr>
<th scope="row">White</th>
<td class="white color">&nbsp;</td>
<td>#ffffff</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>255</td>
<td>255</td>
<td>255</td>
<td class="white color">&nbsp;</td>
</tr>
<tr>
<th scope="row">Black</th>
<td class="black color">&nbsp;</td>
<td>#000000</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>100</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td class="black color">&nbsp;</td>
</tr>
</tbody>
</table>
