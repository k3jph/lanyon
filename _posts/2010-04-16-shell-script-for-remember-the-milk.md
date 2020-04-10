---
id: 682
title: Shell Script for Remember the Milk
date: 2010-04-16T23:00:00-04:00
author: James Howard
layout: post
guid: http://beta.jameshoward.us/2010/04/16/shell-script-for-remember-the-milk/
permalink: /2010/04/16/shell-script-for-remember-the-milk/
dsq_thread_id:
  - "2268152395"
tumblr_howardjp_permalink:
  - http://howardjp.tumblr.com/post/526729497/shell-script-for-remember-the-milk
tumblr_howardjp_id:
  - "526729497"
categories:
  - Blog
tags:
  - geekery
  - GTD
  - Remember the Milk
---
<p>A couple of weeks ago, the <a href="http://www.rememberthemilk.com">Remember the Milk</a> blog posted about <a href="http://blog.rememberthemilk.com/2010/03/tips-tricks-tuesday-two-quick-ways-to-add-tasks-to-remember-the-milk-unix-command-line-automator-service-in-snow-leopard/">adding tasks at the command line</a>.  A simple way to handle task generation, but a bit too complex for even your average Unix hacker.  This script makes it easy and gives you an option to add a note!  Just set RTMADDR and PROG to be your Remember the Milk email address and your local script name, i.o.</p>

<pre><code>#!/bin/sh

RTMADDR='user+NNN@rmilk.com'
PROG='rtm'

TEMP=`getopt -o n --long note -n $PROG -- "$@"`
if [ $? != 0 ] ; then echo "Terminating..." &gt;&amp;2 ; exit 1 ; fi
eval set -- "$TEMP"
while true; do
        case "$1" in
                -n|--note) NOTE='true'; shift;;
                --) shift ; break ;;
                *) help;
        esac
done

if [ x$NOTE == 'x' ]; then
    mailx -s "$1" $RTMADDR &lt; /dev/null &gt; /dev/null
else
    mailx -s "$1" $RTMADDR
fi
</code></pre>

<p>From RTM&#8217;s example,</p>

<pre><code>rtm "Test code changes committed by Bart. ^tom @ 9a !1 #Testing #na @Work"
</code></pre>

<p>And use <code>-n</code> if you&#8217;d like it to ask for a note.</p>
