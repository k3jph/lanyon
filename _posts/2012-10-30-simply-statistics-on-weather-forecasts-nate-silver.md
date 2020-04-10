---
id: 440
title: 'Simply Statistics: On weather forecasts, Nate Silver, and the politicization of statistical illiteracy'
date: 2012-10-30T20:59:27-04:00
author: James Howard
layout: post
guid: http://beta.jameshoward.us/2012/10/30/simply-statistics-on-weather-forecasts-nate-silver/
permalink: /2012/10/30/simply-statistics-on-weather-forecasts-nate-silver/
tumblr_jhresearchlog_permalink:
  - http://jhresearchlog.tumblr.com/post/34654756677/simply-statistics-on-weather-forecasts-nate-silver
tumblr_jhresearchlog_id:
  - "34654756677"
dsq_thread_id:
  - "2262929569"
ampforwp_custom_content_editor_checkbox:
  - ""
categories:
  - Blog
tags:
  - data science
  - innumeracy
  - mathematics
  - R
  - scientific computing
  - statistics
---
<a href='http://simplystatistics.org/post/34635539704/on-weather-forecasts-nate-silver-and-the'>Simply Statistics: On weather forecasts, Nate Silver, and the politicization of statistical illiteracy</a>
<div class="link_description">

<a href="http://simplystatistics.org/post/34635539704/on-weather-forecasts-nate-silver-and-the" class="tumblr_blog">simplystatistics</a>:
<blockquote>
As you know, <a href="http://simplystatistics.org/post/34483703514/sunday-data-statistics-link-roundup-10-28-12" target="_blank">we</a> <a href="http://simplystatistics.org/post/33564003058/sunday-data-statistics-link-roundup-10-14-12" target="_blank">have</a> a <a href="http://simplystatistics.org/post/29407938554/statistics-statisticians-need-better-marketing" target="_blank">thing</a> for <a href="http://simplystatistics.org/post/13684264380/citizen-science-makes-statistical-literacy-critical" target="_blank">statistical literacy</a> here at Simply Stats. So of course this <a href="http://www.politico.com/blogs/media/2012/10/nate-silver-romney-clearly-could-still-win-147618.html" target="_blank">column over at Politico</a> got our attention (via Chris V. and others). The column is an attack on Nate Silver, <a href="http://fivethirtyeight.blogs.nytimes.com/" target="_blank">who has a blog</a> where he tries to predict the outcome of elections in the...</blockquote>
I've revised your code for efficiency:


[code language="r"]
# Set initial parameters
percentObama = 0.505
sdObama = 0.01
n = 1000

# Simulate n elections
simulatedPercentObama = rnorm(n,mean=percentObama,sd=sdObama)

# Calculate the percent of times Obama wins
percentObamaWin = mean(simulatedPercentObama &gt; 0.5)
percentObamaWin
[/code]
</div>
