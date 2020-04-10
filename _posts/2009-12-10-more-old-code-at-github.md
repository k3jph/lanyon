---
id: 694
title: More Old Code at GitHub
date: 2009-12-10T01:09:53-05:00
author: James Howard
layout: post
guid: http://beta.jameshoward.us/2009/12/10/more-old-code-at-github/
permalink: /2009/12/10/more-old-code-at-github/
tumblr_howardjp_permalink:
  - http://howardjp.tumblr.com/post/276811812/more-old-code-at-github
tumblr_howardjp_id:
  - "276811812"
dsq_thread_id:
  - "2888124652"
instant_articles_submission_id:
  - "1187607478022218"
categories:
  - Blog
tags:
  - bsd
  - computer science
  - information technology
  - M-Net
  - software
  - software engineering
  - systems science
  - Unix
  - utilities
  - uwatch
  - write
---
<p>I have recovered from an old <a title="http://en.wikipedia.org/wiki/Iomega_Zip_drive" href="http://Iomega%20Zip%20drive">Iomega Zip disk</a> a few more programs I wrote in the 1997-1998 time frame which may be of some interest:</p>
<ul><li><a title="Daemon at GitHub" href="http://github.com/howardjp/daemon">daemon</a><br />Daemon was originally written for FreeBSD to use the 4.4BSD library function, <a title="Daemon manual page" href="http://www.freebsd.org/cgi/man.cgi?query=daemon&amp;apropos=0&amp;sektion=0&amp;manpath=4.4BSD+Lite2&amp;format=html">daemon(3)</a> to launch a command after disassociating itself from the controlling TTY.  I originally saw such an application on <a title="http://www.arbornet.org" href="http://Arbornet%20/%20M-Net">M-Net</a> which ran BSD/OS 3.1 at the time.  The source was unavailable, but it was easy to reimplement.  Modern Linux implementations now include daemon(3), so it should be usable on Linux today.<br /><br /></li>
<li><a title="rpt at GitHub" href="http://github.com/howardjp/rpt">rpt</a><br />Rpt was based upon the source from daemon, above but instead of disassociating from the controlling terminal, rpt reruns the command at a specified interval.  This allows the user to monitor the output of a program over time.<br /><br /></li>
<li><a title="uwatch at GitHub" href="http://github.com/howardjp/uwatch">uwatch</a><br />Uwatch was also born of M-Net.  M-Net is an interactive BBS system dating back to 1983, which has always allowed users to communicate directly in real time.  As a result, someone once developed a program to notify users when their friends logged in or out.  However, it was always spotty at best, especially during a long session.  I worked extensively on it back in 1997 to solve some memory management issues.  This is what remains of that effort.<br /><br /></li>
<li><a title="write at GitHub" href="http://github.com/howardjp/write">write</a><br />When I was a student at Miami University, we had several Linux systems spread across three (of four) campuses and we occasionally used <a title="write manual page" href="http://www.freebsd.org/cgi/man.cgi?query=write&amp;apropos=0&amp;sektion=0&amp;manpath=Unix+Seventh+Edition&amp;format=html">write(1)</a> to talk to each other.  This implementation of write honors MIT&#8217;s <a title="Project Athena at Wikipedia" href="http://en.wikipedia.org/wiki/Project_Athena">Project Athena</a>'s network-aware write protocol and allows users to send message to users on other systems.</li>
</ul>
