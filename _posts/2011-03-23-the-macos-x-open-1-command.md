---
id: 661
title: The MacOS X open(1) Command
date: 2011-03-23T01:23:12-04:00
author: James Howard
layout: post
guid: http://beta.jameshoward.us/2011/03/23/the-macos-x-open-1-command/
permalink: /2011/03/23/the-macos-x-open-1-command/
dsq_thread_id:
  - "2268135103"
tumblr_howardjp_permalink:
  - http://howardjp.tumblr.com/post/4035306032/the-macos-x-open-1-command
tumblr_howardjp_id:
  - "4035306032"
instant_articles_submission_id:
  - "954340901365189"
categories:
  - Blog
tags:
  - computer science
  - information technology
  - Mac OS
  - shell
  - software engineering
  - systems science
---
<p>MacOS X provides a commnad line tool to open applications and files.  MacOS X applications are actually collections of files residing within one directory with a name ending in <em>.app</em>.  I usually use <strong>open</strong> at the command line to start most applications, leaving the Dock clear of applications not running:</p>

<blockquote>
  <p>howardjp@thermopylae:~$ open /Applications/Safari.app</p>
</blockquote>

<p>is enough to start Safari and if the browser is already running, it will open a new window.</p>

<p>The <strong>open</strong> command also works on individual files and will open the file in its associated application.  For instance, running open on a PDF will open the file in Preview.  And running <strong>open</strong> on a normal directory (as opposed to an application package) will open the directory in Finder.</p>

<p>The <strong>open</strong> command provides a number of useful options.  The option <em>t</em> treats the file, regardless of type, as a text file and opens it in the default text editor.  A related option, <em>e</em> simplifies the process and opens the file in TextEdit, the native text editor provided with MacOS X.  Also related is <em>f</em>, which reads from the standard input and passes the input to the default text editor.</p>

<p>It is also possible to override the default application with other types of files using the option <em>a</em>.  But it is important to remember the full path to the application must be given:</p>

<blockquote>
  <p>open -a /Applications/Adobe Reader 9/Adobe Reader.app/ foo.pdf</p>
</blockquote>

<p>This form is quite cumbersome, but it may be appropriate in some circumstances.  One last option worth mentioning is <em>R</em> which find the references file in Finder, instead of opening the file itself.  Of course, <strong>open</strong> supports other options as well and reveiwing the man page is advised.</p>

<p>Finally, the <strong>open</strong> supports URLs:</p>

<blockquote>
  <p>open <a href="http://www.jameshoward.us">http://www.jameshoward.us</a></p>
</blockquote>

<p>will open my website directly in the default browser.</p>
