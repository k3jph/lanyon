---
id: 680
title: Waterfall Charts in R
date: 2010-05-23T16:07:00-04:00
author: James Howard
layout: post
guid: http://beta.jameshoward.us/2010/05/23/waterfall-charts-in-r/
permalink: /2010/05/23/waterfall-charts-in-r/
dsq_thread_id:
  - "2268152305"
tumblr_howardjp_permalink:
  - http://howardjp.tumblr.com/post/625295781/waterfall-charts-in-r
tumblr_howardjp_id:
  - "625295781"
ampforwp_custom_content_editor_checkbox:
  - ""
instant_articles_submission_id:
  - "780531378766006"
categories:
  - Blog
tags:
  - data science
  - finance
  - graphics
  - mathematics
  - R
  - scientific computing
  - statistics
  - waterfall
---
<p>It is often hard to wrap your head around the finances of organizations and the unusual accounting rules of public organizations make that even more difficult.  When I read <a href="http://books.google.com/books?id=UtNZZU6JLiQC&amp;lpg=PP1&amp;dq=mckinsey%20way&amp;pg=PP1#v=onepage&amp;q&amp;f=false">The McKinsey Way</a> several years ago, I saw the value in using waterfall charts to analyze and understand the finances of public organizations.  So I created functions for plotting waterfall charts using both traditional and grid graphics in <a href="http://www.r-project.org/">R</a>.  Here&#8217;s an example using the sample data from <em>The McKinsey Way</em>:</p>

[caption id="attachment_1874" align="aligncenter" width="480"]<a href="https://jameshoward.us/wp-content/uploads/2010/05/tumblr_l2tyqg9LdU1qzy7qe.png"><img src="https://jameshoward.us/wp-content/uploads/2010/05/tumblr_l2tyqg9LdU1qzy7qe.png" alt="Raisel&#039;s waterfall plot example" width="480" height="480" class="size-full wp-image-1874" /></a> Raisel's waterfall plot example[/caption]

<p>More advanced examples are available in the package demo.  I had intended to write the documentation and submit it as a code snippet to the <a href="http://www.jstatsoft.org/">Journal of Statistical Software</a>.  However, I have yet to actually write the documentation and it is probably not appropriate for JSS, anyway.  Otherwise, the package is complete and is <a href="http://cran.r-project.org/web/packages/waterfall/index.html">now available from CRAN</a>.  The source code <a href="http://bitbucket.org/howardjp/waterfall">is available from Bitbucket</a>.  The code repository contains the outline of an <a href="http://www.eclipse.org/">Eclipse</a> project using <a href="http://www.walware.de/goto/statet">StatET</a>, which I recommend for working with this and all other R packages.</p>
