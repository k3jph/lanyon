---
id: 687
title: PWCrypt is Now at Bitbucket
date: 2010-01-28T14:52:00-05:00
author: James Howard
layout: post
guid: http://beta.jameshoward.us/2010/01/28/pwcrypt-is-now-at-bitbucket/
permalink: /2010/01/28/pwcrypt-is-now-at-bitbucket/
dsq_thread_id:
  - "2309664517"
tumblr_howardjp_permalink:
  - http://howardjp.tumblr.com/post/357967476/pwcrypt-is-now-at-bitbucket
tumblr_howardjp_id:
  - "357967476"
categories:
  - Blog
tags:
  - bitbucket
  - hash
  - Mercurial
  - Netscape
  - password
  - pwcrypt
  - source code
---
<p>As part of my plan to rescue data from old <a href="http://www.nongnu.org/cvs/">CVS</a> repositories, <a href="http://bitbucket.org/howardjp/pwcrypt/">PWCrypt is now available at Bitbucket</a>.  PWCrypt provides command line access to the Unix <a href="http://en.wikipedia.org/wiki/Crypt_%28Unix%29#Library_Function">crypt library function</a>.</p>

<p>This program and an accompanying article were written in response to a problem I had in 1999 with Netscape Enterprise Server.  After taking over administration of a Windows NT-based Netscape server, I discovered I did not know the administrator password for NES.  I hunted down the password file and saw it hashed passwords using the same format at the password file for Unix-like systems.</p>

<p>So I needed a hashed value for a known password to drop into NES&#8217;s password database and used this program to create that value.  It&#8217;s seen no substantive changes since the original publication eleven years ago.</p>

<p>Nota bene:  This is a <a href="http://mercurial.selenic.com/">Mercurial</a> repository stored on <a href="http://www.bitbucket.org">Bitbucket</a>, not Git/GitHub like I&#8217;ve made available the past few weeks.  I chose Mercurial for this project so I could get a better feeling for it vis-à-vis Git.</p>
