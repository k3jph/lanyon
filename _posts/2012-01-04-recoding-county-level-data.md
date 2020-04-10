---
id: 451
title: Recoding County-Level Data
date: 2012-01-04T02:41:00-05:00
author: James Howard
layout: post
guid: http://beta.jameshoward.us/2012/01/04/recoding-county-level-data-2/
permalink: /2012/01/04/recoding-county-level-data/
tumblr_jhresearchlog_permalink:
  - http://jhresearchlog.tumblr.com/post/30315034259/recoding-county-level-data
tumblr_jhresearchlog_id:
  - "30315034259"
dsq_thread_id:
  - "2262924197"
ampforwp_custom_content_editor_checkbox:
  - ""
instant_articles_submission_id:
  - "1860237564247440"
categories:
  - Blog
tags:
  - counties
  - data
  - data science
  - environmental policy
  - environmental studies
  - FEMA
  - flood mitigation
  - flood studies
  - mathematics
  - scientific computing
---
This evening I finished recoding a list of grants from <a href="http://www.fema.gov">FEMA</a> for <a href="http://www.fema.gov/government/grant/fma/index.shtm">Flood Mitigation Assistance</a>. This dataset contains 2108 entries, and contains the following columns, among others:

<table border="0"><tbody><tr><th style="border-bottom: 1px solid black;border-top: 2px solid black;border-right: 10px solid transparent">State</th>
      <th style="border-bottom: 1px solid black;border-top: 2px solid black;border-right: 10px solid transparent">County</th>
      <th style="border-bottom: 1px solid black;border-top: 2px solid black">Subgrantee</th>
    </tr><tr><td style="border-right: 10px solid transparent">Maryland</td>
      <td style="border-right: 10px solid transparent">Garrett</td>
      <td>Oakland, Town Of</td>
    </tr><tr><td style="border-right: 10px solid transparent">Maryland</td>
      <td style="border-right: 10px solid transparent"></td>
      <td>Town of Bel Air</td>
    </tr><tr><td style="border-right: 10px solid transparent">Maryland</td>
      <td style="border-right: 10px solid transparent"></td>
      <td>Howard County Department of Fire Rescue Services</td>
    </tr><tr><td style="border-bottom: 2px solid black;border-right: 10px solid transparent">Maryland</td>
      <td style="border-bottom: 2px solid black;border-right: 10px solid transparent">Worcester</td>
      <td style="border-bottom: 2px solid black">Ocean City, Town Of</td></tr></tbody></table>

Because many of the subgrantee fields are filled even when the county is not and most of the subgrantees are local government agencies, I tried to recode the counties according to FIPS 6-4, &#8220;Counties and Equivalent Entities of the United States, Its Possessions, and Associated Areas.&#8221;   Local governments were recoded to their parent counties, as appropriate.

Going through this process by hand, I have some observations on the first-order divisions of states:

<ol><li>There are five townships in Ohio with the name Scioto.</li>
<li>There are two counties named Jeff Davis, one named Jefferson Davis, and a parish in Louisiana named Jefferson Davis.</li>
<li>There are seven counties in the United States named Howard County.</li>
<li>A remarkable number of states have cities and counties with the same name, but which are not near each other.</li>
</ol>
