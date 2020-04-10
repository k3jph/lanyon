---
id: 2407
title: Stop Making 3D Plots
date: 2015-08-12T08:49:25-04:00
author: James Howard
layout: post
guid: https://jameshoward.us/?p=2407
permalink: /2015/08/12/stop-making-3d-plots/
tc-thumb-fld:
  - 'a:2:{s:9:"_thumb_id";s:4:"2408";s:11:"_thumb_type";s:5:"thumb";}'
dsq_thread_id:
  - "4025721114"
ampforwp_custom_content_editor_checkbox:
  - null
instant_articles_submission_id:
  - "1380816451981770"
onesignal_meta_box_present:
  - "1"
onesignal_send_notification:
  - ""
php_everywhere_code:
  - 'Just put [php_everywhere] where you want the code to be executed.'
ampforwp_custom_content_editor:
  - ""
ampforwp-amp-on-off:
  - default
featured-image: XKCD-Self-Description.png
categories:
  - Blog
tags:
  - data science
  - math education
  - mathematics
  - scientific computing
  - statistics
  - visualization
---
[FlowingData](http://flowingdata.com/2015/08/11/real-chart-rules-to-follow/) gave a list of charting rules to follow.  I disagree with one, in that pie charts are never acceptable because it is difficult to perceive the differences in size between one pie chart and another.  This is especially true in 3D plots.  Take this plot, for instance:

<img src="https://jameshoward.us/wp-content/uploads/2015/08/samplepiechart.png" alt="samplepiechart" width="1504" height="904" class="aligncenter size-full wp-image-2410" />

In this plot, despite the fact there are an equal number of oranges and kiwi (25), the oranges section of the plot is about twice as large as the kiwi section.  Think of it in these terms:  When a plot is printed, a good plot will use twice as much ink to represent a value twice as large and use the same amount of ink to represent the same value.

This is often a problem I see when teaching the statistical portion of [Finite Mathematics](/teaching/mathematics) or statistics.  During the plotting portion, students will try to make fancier and fancier graphics, and that just doesn't help the case.  So turn off the 3D and avoid the pie chart.  There's nothing a pie chart can do a bar chart doesn't do better:

<img src="https://jameshoward.us/wp-content/uploads/2015/08/samplebarchart.png" alt="samplebarchart" width="1504" height="904" class="aligncenter size-full wp-image-2409" />

_Image by [Randall Munroe / xkcd](https://xkcd.com/688/)...now that's an effective use of ink._
