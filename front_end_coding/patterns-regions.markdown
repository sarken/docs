---
layout: front_end_guide
title: Diagrams of Regions
---
While the regions aren't themselves reusable patterns -- each region appears a maximum of once per page -- they do make use of patterns.

* [Regions overview](#regions-overview)
* [Header region](#header-region)
    * [Log in block](#header-region-log-in-block)
    * [Greeting block](#header-region-greeting-block)
* [Dashboard region](#dashboard-region)
* [Main region](#main-region)
* [Footer region](#footer-region)

<h3 id="regions-overview">Regions overview</h3>

The five regions are contained within two wrappers. The outer wrapper surrounds all five regions, while the inner wrapper surrounds the main and dashboard regions.

<div class="diagram">
  <ol>
    <li>
      <code>&lt;body&gt;</code>
      <ol>
        <li>
          <code>&lt;div id="outer" class="wrapper"&gt;</code>
          <ol>
            <li>
              <code>&lt;ul id="skiplinks"&gt;</code>
            </li>
            <li>
              <code>&lt;div id="header" class="region"&gt;</code>
            </li>
            <li>
              <code>&lt;div id="inner" class="wrapper"&gt;</code>
              <ol>
                <li>
                  <code>&lt;div id="dashboard" class="region"&gt;</code>
                </li>
                <li>
                  <code>&lt;div id="main" class="dashboard region"&gt;</code>
                </li>
              </ol>
            </li>
            <li>
              <code>&lt;div id="footer" class="region"&gt;</code>
            </li>
          </ol>
        </li>
      </ol>
    </li>
  </ol>
</div>

<h3 id="header-region">Header region</h3>

The header is the first region, styled in [ 13-group-blurb.css](https://github.com/otwcode/otwarchive/blob/master/public/stylesheets/site/2.0/03-region-header.css). It contains our branding, the main navigation, and depending on whether or not you are logged in, the log in or greeting block.

<div class="diagram">
  <ol>
    <li>
      <code>&lt;div id="header" class="region"&gt;</code>
      <ol>
        <li>
          <code>&lt;h1 class="heading"&gt;</code>
            <ol>
              <li>
                <code>&lt;a&gt;</code>
                <ol>
                  <li>
                    <code>&lt;span&gt;</code>
                  </li>
                  <li>
                    <code>&lt;sup&gt;</code>
                  </li>
                  <li>
                    <code>&lt;img&gt;</code>
                  </li>
                </ol>
              </li>
            </ol>
          </li>
        <li>log in or greeting block</li>
        <li>
          <code>&lt;h3 class="landmark heading"&gt;</code>
        </li>
        <li>
          <code>&lt;ul class="primary navigation actions"&gt;</code>
          <ol>
            <li>
              <code>&lt;li class="dropdown"&gt;</code>
              <ol>
                <li>
                  <code>&lt;a class="dropdown-toggle"&gt;</code>
                </li>
                <li>
                  <code>&lt;ul class="menu dropdown-menu"&gt;</code>
                  <ol>
                    <li>
                      <code>&lt;li&gt;</code>
                      <ol>
                        <li>
                          <code>&lt;a&gt;</code>
                        </li>
                      </ol>
                    </li>
                    <li>
                      <code>&lt;li&gt;</code>
                      <ol>
                        <li>
                          <code>&lt;a&gt;</code>
                        </li>
                      </ol>
                    </li>
                    <li>...</li>
                  </ol>
                </li>
              </ol>
            </li>
            <li>
              <code>&lt;li class="search"&gt;</code>
              <ol>
                <li>
                  <code>&lt;form id="search" class="search"&gt;</code>
                  <ol>
                    <li>
                      <code>&lt;fieldset&gt;</code>
                      <ol>
                        <li>
                          <code>&lt;legend&gt;</code>
                        </li>
                        <li>
                          <code>&lt;p&gt;</code>
                          <ol>
                            <li>
                              <code>&lt;label class="landmark"&gt;</code>
                            </li>
                            <li>
                              <code>&lt;input id="site_search" class="text" type="text"&gt;</code>
                            </li>
                            <li>
                              <code>&lt;span class="tip"&gt;</code>
                            </li>
                            <li>
                              <code>&lt;span class="submit actions"&gt;</code>
                              <ol>
                                <li>
                                  <code>&lt;input class="button" type="submit"&gt;</code>
                                </li>
                              </ol>
                            </li>
                          </ol>
                        </li>
                      </ol>
                    </li>
                  </ol>
                </li>
              </ol>
            </li>
          </ol>
        </li>
        <li>
          <code>&lt;div class="clear"&gt;</code>
        </li>
      </ol>
    </li>
  </ol>
</div>

The hyphenated class names are not in the view files and are only applied when the user has JavaScript enabled; therefore, they should not be used for styling the header elements.

<h4 id="header-region-log-in-block">Log in block</h4>

The log in block consists of a link that summons the small log in form when the user has JavaScript enabled or that takes the user to the log in page when they have JavaScript disabled.

<div class="diagram">
  <ol>
    <li>
      <code>&lt;div id="login" class="dropdown"&gt;</code>
      <ol>
        <li>
          <code>&lt;p class="user actions"&gt;</code>
          <ol>
            <li>
              <code>&lt;a class="dropdown-toggle"&gt;</code>
            </li>
          </ol>
        </li>
        <li>
          <code>&lt;div id="small_login" class="simple login"&gt;</code>
          <ol>
            <li>
              <code>&lt;form id="new_user_session"&gt;</code>
              <ol>
                <li>
                  <code>&lt;dl&gt;</code>
                  <ol>
                    <li>
                      <code>&lt;dt&gt;</code>
                      <ol>
                        <li>
                          <code>&lt;label&gt;</code>
                        </li>
                      </ol>
                    </li>
                    <li>
                      <code>&lt;dd&gt;</code>
                      <ol>
                        <li>
                          <code>&lt;input class="text" type="text"&gt;</code>
                        </li>
                      </ol>
                    </li>
                    <li>
                      <code>&lt;dt&gt;</code>
                      <ol>
                        <li>
                          <code>&lt;label&gt;</code>
                        </li>
                      </ol>
                    </li>
                    <li>
                      <code>&lt;dd&gt;</code>
                      <ol>
                        <li>
                          <code>&lt;input class="text" type="text"&gt;</code>
                        </li>
                      </ol>
                    </li>
                  </ol>
                </li>
                <li>
                  <code>&lt;p class="submit actions"&gt;</code>
                  <ol>
                    <li>
                      <code>&lt;label class="action"&gt;</code>
                      <ol>
                        <li>
                          <code>&lt;input type="checkbox"&gt;</code>
                        </li>
                      </ol>
                    </li>
                    <li>
                      <code>&lt;input type="submit"&gt;</code>
                    </li>
                  </ol>
                </li>
                <li>
                  <code>&lt;ul class="footnote actions"&gt;</code>
                  <ol>
                    <li>
                      <code>&lt;li&gt;</code>
                      <ol>
                        <li>
                          <code>&lt;a&gt;</code>
                        </li>
                      </ol>
                    </li>
                    <li>
                      <code>&lt;li&gt;</code>
                      <ol>
                        <li>
                          <code>&lt;a&gt;</code>
                        </li>
                      </ol>
                    </li>
                  </ol>
                </li>
              </ol>
            </li>
          </ol>
        </li>
      </ol>
    </li>
  </ol>
</div>

<h4 id="header-region-greeting-block">Greeting block</h4>

The greeting block contains the user's icon and navigation items that are only available to logged in users.

<div class="diagram">
  <ol>
    <li>
      <code>&lt;div id="greeting"&gt;</code>
      <ol>
        <li>
          <code>&lt;h3 class="landmark heading"&gt;</code>
        </li>
        <li>
          <code>&lt;ul class="user navigation actions"&gt;</code>
          <ol>
            <li>
              <code>&lt;li class="dropdown"&gt;</code>
              <ol>
                <li>
                  <code>&lt;a class="dropdown-toggle"&gt;</code>
                </li>
                <li>
                  <code>&lt;ul class="menu dropdown-menu"&gt;</code>
                  <ol>
                    <li>
                      <code>&lt;li&gt;</code>
                      <ol>
                        <li>
                          <code>&lt;a&gt;</code>
                        </li>
                      </ol>
                    </li>
                  </ol>
                </li>
              </ol>
            </li>
            <li>
              <code>&lt;li class="dropdown"&gt;</code>
              <ol>
                <li>
                  <code>&lt;a class="dropdown-toggle"&gt;</code>
                </li>
                <li>
                  <code>&lt;ul class="menu dropdown-menu"&gt;</code>
                  <ol>
                    <li>
                      <code>&lt;li&gt;</code>
                      <ol>
                        <li>
                          <code>&lt;a&gt;</code>
                        </li>
                      </ol>
                    </li>
                    <li>
                      <code>&lt;li&gt;</code>
                      <ol>
                        <li>
                          <code>&lt;a&gt;</code>
                        </li>
                      </ol>
                    </li>
                  </ol>
                </li>
              </ol>
            </li>
            <li>
              <code>&lt;li&gt;</code>
              <ol>
                <li>
                  <code>&lt;a&gt;</code>
                </li>
              </ol>
            </li>
          </ol>
        </li>
        <li>
          <code>&lt;p class="icon"&gt;</code>
          <ol>
            <li>
              <code>&lt;a&gt;</code>
              <ol>
                <li>
                  <code>&lt;img class="icon"&gt;</code>
                </li>
              </ol>
            </li>
          </ol>
        </li>
      </ol>
    </li>
  </ol>
</div>

<h3 id="dashboard-region">Dashboard region</h3>

The dashboard is the second region, styled in [ 04-region-dashboard.css](https://github.com/otwcode/otwarchive/blob/master/public/stylesheets/site/2.0/04-region-dashboard.css). It does not appear on every page, but when it *is* on the page, it comes after the header and before the main region.

<div id="diagram">
  <ol>
    <li>
      <code>&lt;div id="dashboard" class="region"&gt;</code>
      <ol>
        <li>
          <code>&lt;h4 class="landmark heading"&gt;</code>
        </li>
        <li>
          <code>&lt;ul class="navigation actions"&gt;</code>
          <ol>
            <li>
              <code>&lt;li&gt;</code>
              <ol>
                <li>
                  <code>&lt;a&gt;</code>
                </li>
              </ol>
            </li>
            <li>
              <code>&lt;li&gt;</code>
              <ol>
                <li>
                  <code>&lt;a&gt;</code>
                </li>
              </ol>
            </li>
            <li>
              <code>&lt;li&gt;</code>
              <ol>
                <li>
                  <code>&lt;span class="current"&gt;</code>
                </li>
              </ol>
            </li>
          </ol>
        </li>
        <li>
          <code>&lt;h4 class="landmark heading"&gt;</code>
        </li>
        <li>
          <code>&lt;ul class="navigation actions"&gt;</code>
        </li>
      </ol>
    </li>
  </ol>
</div>

<h3 id="main-region">Main region</h3>

The structure of `#main` varies significantly from page to page. Most of the remaining style sheets deal with elements found in main; the [ 05-region-main.css](https://github.com/otwcode/otwarchive/blob/master/public/stylesheets/site/2.0/05-region-main.css) style sheet only covers very basic styles, like how wide it should be when appearing with a dashboard.

<h3 id="footer-region">Footer region</h3>

The footer is the final region, and its styles are in [ 06-region-footer.css](https://github.com/otwcode/otwarchive/blob/master/public/stylesheets/site/2.0/06-region-footer.css).

<div class="diagram">
  <ol>
    <li>
      <code>&lt;div id="footer" class="region"&gt;</code>
      <ol>
        <li>
          <code>&lt;h3 class="landmark heading"&gt;</code>
        </li>
        <li>
          <code>&lt;ul class="navigation actons"&gt;</code>
          <ol>
            <li>
              <code>&lt;li class="module group"&gt;</code>
                <ol>
                  <li>
                    <code>&lt;h4 class="heading"&gt;</code>
                    <ol>
                      <li>
                        <code>&lt;ul class="menu"&gt;</code>
                        <ol>
                          <li>
                            <code>&lt;li&gt;</code>
                            <ol>
                              <li>
                                <code>&lt;a&gt;</code>
                              </li>
                            </ol>
                          </li>
                        </ol>
                      </li>
                      <li>
                        <code>&lt;ul class="menu"&gt;</code>
                      </li>
                    </ol>
                  </li>
                </ol>
              </li>
              <li>
                <code>&lt;li class="module group"&gt;</code>
              </li>
            </ol>
          </li>
        </li>
      </ol>
    </li>
  </ol>           
</div>