---
id: 2036
title: Matrix Row Echelon Form in R
date: 2015-04-20T18:43:56-04:00
author: James Howard
layout: post
guid: https://jameshoward.us/?p=2036
permalink: /2015/04/20/matrix-row-echelon-form-in-r/
dsq_thread_id:
  - "3698542940"
ampforwp_custom_content_editor_checkbox:
  - ""
featured-image: matrices-840x525.jpg
categories:
  - Blog
tags:
  - CMNA
  - data science
  - linear algebra
  - linear equations
  - mathematics
  - matrix algebra
  - numerical analysis
  - R
  - scientific computing
---
For reasons unknown, I can't find a function to transform a matrix into row echelon form in R.  There's a function on Rosetta Code for <a href="http://rosettacode.org/wiki/Reduced_row_echelon_form#R">reduced row echelon form</a> in R.  So I wrote this on Sunday.  And if you look at this and the Rosetta Code solution, they work in mostly the same way.  This will be released as part of a larger package later, with documentation and unit tests.  But it's useful enough to stand on its own here.

[sourcecode language="R"]
refmatrix &lt;- function(m) {
    count.rows &lt;- nrow(m)
    count.cols &lt;- ncol(m)
    piv &lt;- 1
    
    for(row.curr in 1:count.rows) {
        if(count.cols &gt; piv) {
            i &lt;- row.curr
            while(m[i, piv] == 0) {
                i &lt;- i + 1
                if(count.rows == i) {
                    i &lt;- row.curr
                    piv &lt;- piv + 1
                    if(count.cols == piv)
                        return(m)
                }
            }
            m &lt;- swaprows(m, row.curr, i)
            for(j in row.curr:count.rows)
                if(j != row.curr) {
                    k &lt;- m[j, piv] / m[row.curr, piv]
                    m &lt;- replacerow(m, row.curr, j, k)
                }
            piv &lt;- piv + 1
        }
    }
    return(m)
}

swaprows &lt;- function(m, row1, row2) {
    row.tmp &lt;- m[row1,]
    m[row1,] &lt;- m[row2,]
    m[row2,] &lt;- row.tmp

    return(m)
}

replacerow &lt;- function(m, row1, row2, k) {
    m[row2,] &lt;- m[row2,] - m[row1,] * k
    return(m)
}
[/sourcecode]

<em>Image by <a href="https://www.flickr.com/photos/vialbost/16084697841">Frédérique Voisin-Demery</a>.</em>
