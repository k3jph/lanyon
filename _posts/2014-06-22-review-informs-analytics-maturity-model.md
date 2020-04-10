---
id: 1335
title: Review of the INFORMS Analytics Maturity Model
date: 2014-06-22T11:00:51-04:00
author: James Howard
layout: post
guid: http://jameshoward.us/?p=1335
permalink: /2014/06/22/review-informs-analytics-maturity-model/
dsq_thread_id:
  - "2786359154"
ampforwp_custom_content_editor_checkbox:
  - ""
instant_articles_submission_id:
  - "210643759412219"
categories:
  - Blog
tags:
  - business
  - data science
  - mathematics
  - scientific computing
  - statistics
---
[caption id="attachment_1338" align="aligncenter" width="1280"]<a href="https://jameshoward.us/wp-content/uploads/2014/06/54997131_6b8171eb75_o.jpg"><img src="https://jameshoward.us/wp-content/uploads/2014/06/54997131_6b8171eb75_o.jpg" alt="Tell me again which one tells me what I need to know? (Andy Fogg / Flickr)" width="1280" height="1024" class="size-full wp-image-1338" /></a> Tell me again which one tells me what I need to know? (Andy Fogg / Flickr)[/caption]

At last Monday's WINFORMS meetup in DC, Aaron Burciaga and Raj Reddi presented the new INFORMS <a href="https://analyticsmaturity.informs.org/">Analytics Maturity Model</a> (AMM).  The AMM is a graded typology allowing organizations to assess their use of data analytics in existing business processes.  The AMM also gives organizations the ability to set goals for future performance.  Burciaga and Reddi's presentation covered the basics of the model and presented viewers with the website, which can track organizational performance over time.  Such maturity models give organizations tools to match their performance against a best practices framework.

These types of maturity models have become <em>de rigueur</em> in information technology since the Carnegie Mellon and the Department of Defense released <a href="http://whatis.cmmiinstitute.com/">Capability Maturity Model Integration</a> (CMMI).  Since then, maturity models have proliferated and many organizations are releasing their own for data analytics.  <a href="http://www.cardinalpath.com/services/online-analytics-maturity-model/">CardinalPath</a>, <a href="http://myanalyticsscore.com/">Adobe</a>, <a href="http://www.accenture.com/us-en/landing-pages/accenture-analytics/Pages/data-insights-analytics-roi.aspx">Accenture</a>, <a href="https://www.google.com/search?q=analytics+maturity+model">among others</a>, have all released analytics maturity models.  Some of these are industry specific, such as health care.  Others are targeted at specific functional areas, such as marketing.  The AMM is a generalist model for analytical maturity.

Having looked at a number of similar systems over time, my great complaint with the AMM from INFORMS is its unnecessary complexity and ill-defined specification.  The unnecessary complexity comes from measuring 12 different dimensions of analytics maturity at 10 performance levels.  For comparison, the <a href="http://www.sas.com/resources/whitepaper/wp_6426.pdf">SAS analytical maturity model</a> measures 5 dimensions at 6 levels and the <a href="http://www.boozallen.com/media/file/The-Field-Guide-to-Data-Science.pdf">Booz Allen Hamilton</a>'s uses 5 levels across 1 dimension (though there are some complications here).  Others vary but are usually simpler than the INFORMS AMM.  The complexity leads to questions that are out of place within a maturity model, e.g:

<blockquote>
  To what degree are analytics professionals certified, deployed, integrated, and used?
</blockquote>

or

<blockquote>
  To what extent do you maintain a data and analytics quality assurance program across the organization?
</blockquote>

Both of these, and several other questions on the INFORMS AMM specifically address the wrong end of the business process.  Maturity models should be measuring outcomes, not inputs.  This is similar to goals and objectives supporting strategic plans.  An organization cannot measure performance by looking at how much is spent, but only in what is gained.  Similarly, a maturity model should do the same.  The questions above are like asking "Did you hire someone to do the job?" when the correct question to ask is, "Did the job get done?"

This problem is subtle and complex and cannot be resolved without thoroughly revising the AMM as currently presented.  A simpler problem is how performance is the general complexity of the model.  The maturity model uses a 10-tiered graduated scale across all 12 dimensions.  For comparison, the <a href="http://www.sas.com/resources/whitepaper/wp_6426.pdf">SAS Analytical Maturity Assessment</a> measures five dimensions on a six-point scale.  <a href="http://www.boozallen.com/media/file/The-Field-Guide-to-Data-Science.pdf">Booz Allen Hamilton</a>'s model uses a five-point scale on one dimension, though there is some buried complexity there.

But the increased complexity impairs the model's usability in the case of INFORMS.  The model presents 10-tiers grouped under three high-level descriptions:

<ul>
<li>Beginning: 1, 2, and 3</li>
<li>Developing: 4, 5, 6, and 7</li>
<li>Advanced: 8, 9, and 10</li>
</ul>

These descriptive terms are good and come with associated points that illustrate the differences between, say, developing and advanced.  However, there is no explanation of the differences between, for instance, a 5 and 6.  Because there is no delineation, two different people may rate different organizations on essentially different scales.  Two different people could even rate the same organization differently.  This hampers the goal of using the maturity model to further best practices.  As a report card, its value comes in being able to compare an organization to itself at different points in time or to other comparable organizations.

Despite these problems with the model, INFORMS has produced a nice website for tracking current measurements and goals for future evaluations.  The website includes the ability to track action items, record status over time, and produce reports showing the organization and where it fits amongst its peers.  Generally speaking, the website is good and functional and, importantly, usable.

However, the well-implemented website cannot save the model.  The INFORMS AMM measures too much of the wrong things in undefined ways.  Most organizations will not need this type of maturity model to analyze their capabilities.  Those organizations that do will be better served with a simpler, leaner, and cleaner maturity model that tracks what the organization needs.
