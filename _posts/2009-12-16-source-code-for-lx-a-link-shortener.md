---
id: 693
title: Source Code for LX, a Link Shortener
date: 2009-12-16T22:54:43-05:00
author: James Howard
layout: post
guid: http://beta.jameshoward.us/2009/12/16/source-code-for-lx-a-link-shortener/
permalink: /2009/12/16/source-code-for-lx-a-link-shortener/
tumblr_howardjp_permalink:
  - http://howardjp.tumblr.com/post/286614416/source-code-for-lx-a-link-shortener
tumblr_howardjp_id:
  - "286614416"
dsq_thread_id:
  - "2734392082"
instant_articles_submission_id:
  - "1741801862808471"
categories:
  - Blog
tags:
  - cakephp
  - computer science
  - Facebook
  - Google
  - information technology
  - links
  - PHP
  - software
  - software engineering
  - source
  - systems science
  - web
---
<p>Last August, I began work on a link shortening service as a me-too kind of project.  In my case, I wanted to provide custom domains, so that, for instance, <i>The Washington Post</i> could be wp.ly.  However, I had been displeased in the user interface I had created and had not taken it live.</p>
<p>On Monday, the jig was up when both <a title="Making URLs shorter for Google Toolbar and FeedBurner" href="http://googleblog.blogspot.com/2009/12/making-urls-shorter-for-google-toolbar.html">Google</a> and <a title="Facebook Testing New URL Shortener, fb.me" href="http://www.insidefacebook.com/2009/12/14/facebook-testing-new-url-shortener-fb-me/">Facebook</a> pushed their own link shorteners into the arena.  Additionally, bit.ly announced <a title="Announcing bit.ly Pro" href="http://blog.bit.ly/post/284009728/announcing-bit-ly-pro">bit.ly Pro</a> which will provide the custom domain I had been interested in.  Rather than being steamrolled by these behemoths, I will instead open source my code under a <a href="http://en.wikipedia.org/wiki/BSD_licenses">BSD License</a>.  It is now available at <a title="lx at GitHub" href="http://github.com/howardjp/lx">GitHub</a>.</p>
<p>From the readme:</p>
<p>lx is a URL-shortening application created in CakePHP.  The Git repository is a top-skimming of the <code>/app</code> directory from CakePHP v1.2.4.  Also included in <code>/sql</code> is a database template for PostgreSQL.  <i>It is important to note, this code does not work and will need significant revision before being functional.</i> However, here is a partial list of partially implemented features:</p>
<ul><li>URL addition</li>
<li>URL deletion</li>
<li>URL redirection</li>
<li>URL favoriting (through the &#8220;stars&#8221; concept)</li>
<li>User accounts</li>
<li>User verification</li>
<li>URL renaming (title, not target)</li>
<li>Some jQuery-based AJAX</li>
</ul><p>Please use this as the basis for your own work.  If you wish to contribute changes back, please do.</p>
