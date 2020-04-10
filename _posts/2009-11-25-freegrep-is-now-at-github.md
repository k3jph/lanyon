---
id: 696
title: FreeGrep is now at GitHub
date: 2009-11-25T03:42:44-05:00
author: James Howard
layout: post
guid: http://beta.jameshoward.us/2009/11/25/freegrep-is-now-at-github/
permalink: /2009/11/25/freegrep-is-now-at-github/
dsq_thread_id:
  - "2492969275"
tumblr_howardjp_permalink:
  - http://howardjp.tumblr.com/post/256440573/freegrep-is-now-at-github
tumblr_howardjp_id:
  - "256440573"
instant_articles_submission_id:
  - "1624704571165711"
categories:
  - Blog
tags:
  - bsd
  - c
  - computer science
  - FreeBSD
  - FreeGrep
  - grep
  - information technology
  - NetBSD
  - OpenBSD
  - software
  - software engineering
  - systems science
  - UMD
---
<p>I have been learning to use <a title="Git" href="http://git-scm.com/">Git</a>, the distributed version control system.  I am more than a bit familiar with both <a title="CVS - Concurrent Versions System" href="http://www.nongnu.org/cvs/">CVS</a> and <a title="Subversion" href="http://subversion.tigris.org/">Subversion</a>, and finding Git to be interesting and capable of some incredible feats of source management.  But when working with new tools, it is often easier to find non-trivial examples upon which to experiment.  This brings us to FreeGrep.</p>
<p>Back in July of 1999, I was between freshman and sophomore years as a <a title="University of Maryland Department of Computer Science" href="http://www.cs.umd.edu">computer science</a> major at the <a title="University of Maryland, College Park" href="http://www.umd.edu">University of Maryland</a> (when returning a month later, I switched to the <a title="University of Maryland Department of Mathematics" href="http://www.math.umd.edu">Department of Mathematics</a>). When you are a compsci major, you tend to get excited over things like the <a title="Towers of Hanoi" href="http://en.wikipedia.org/wiki/Tower_of_Hanoi">Towers of Hanoi</a> problem, <a title="self-balancing binary search trees" href="http://en.wikipedia.org/wiki/Self-balancing_binary_search_tree">self-balancing binary search trees</a>, or <a title="NP-complete" href="http://en.wikipedia.org/wiki/NP-complete">NP-completeness</a>.  Back then, what got me going were <a title="Finite-state machine" href="http://en.wikipedia.org/wiki/Finite-state_machine">finite state automata</a>. One in particular, called the <a title="Boyer-Moore string search algorithm" href="http://en.wikipedia.org/wiki/Boyer-Moore_string_search_algorithm">Boyer-Moore search algorithm</a> caught my attention.  (Also, see item 179 in <a title="HAKMEM via FTP" href="ftp://publications.ai.mit.edu/ai-publications/pdf/AIM-239.pdf">HAKMEM</a>.)</p>
<p>I had used <a title="FreeBSD" href="http://www.freebsd.org">FreeBSD</a>, the 4.4BSD-derived operating system for several years, finding it to be a sane and sensible alternative to the madness that surrounded the Linux development process, especially ten years ago.  A number of the tools used in 4.4BSD-derived operating systems, especially toolchain components, are the GNU versions, leading to more <a title="University of California, Berkeley advertising clause" href="http://en.wikipedia.org/wiki/BSD_licences#UC_Berkeley_advertising_clause">licensing holy wars</a> than necessary (and I can keep up with).  So with toys-a-plenty, and some fancy-pants education, I took to writing my own version of <a title="grep" href="http://www.opengroup.org/onlinepubs/9699919799/utilities/grep.html">grep(1)</a>, a regular expression pattern matcher and cornerstone of any respectable Unix-like operating system.  I posted an <a title="Repalcement for grep(1)" href="http://www.mail-archive.com/freebsd-hackers@freebsd.org/msg00572.html">initial announcement</a> to the FreeBSD Hackers mailing list (with a disturbingly misspelled subject line) where I expressed my hope it would someday be the version shipped with FreeBSD.  I had barely scratched the surface of the problem, but a few others were inspired and patches started flying across the world with incredible alacrity.  Source control was nowhere to be seen, but it was just for fun, anyway.  As the summer wound down, I worked less and less on the program.  It was almost completely correct but was terribly slow in <a title="Replacing GNU grep revisited (Christopher Weimann)" href="http://monkey.org/freebsd/archive/freebsd-hackers/200306/msg00516.html">some pathological cases</a>.</p>
<p>For reasons I can no longer recall, on September 14, 2002, created a new CVS repository and checked in FreeGrep v0.16.  And in early 2003, a man named <a title="Sean Farley" href="http://www.farley.org/">Sean Farley</a> contacted me with some patches.  I committed them to my repository, but never cut a new release.  But later that year, both the <a title="The NetBSD Project" href="http://www.netbsd.org">NetBSD</a> and <a title="The OpenBSD Project" href="http://www.openbsd.org">OpenBSD</a> projects dropped GNU grep from their source trees and added FreeGrep v0.16 and started doing a lot of heavy work, dramatically increasing the speed and solving many lingering bugs in the code.  I watched, but did not say much.</p>
<p>Because FreeGrep is a small program (2121 SLOC in the current release of OpenBSD, the largest implementation) with a complex development history, it was the perfect place to experiment with Git.  So this week, I used Git&#8217;s CVS import feature to import my CVS tree, the OpenBSD CVS tree, and the NetBSD CVS tree into one repository.  Now, the full history from these development strands are available and I did the obvious thing and merged work done by the OpenBSD project directly into the master branch and consider it the new base.  Because I have been occasionally remiss in keeping this code available to all, I have uploaded everything I have, including fifteen pre-CVS source releases to <a title="FreeGrep at GitHub" href="http://github.com/howardjp/freegrep">GitHub</a> where it can remain available to any interested party.  Please enjoy.</p>
<p>And submit patches.</p>
