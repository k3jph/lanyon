---
id: 3325
title: Numerical Analysis talk at Statistical Programming DC
date: 2015-12-09T00:01:55-05:00
author: James Howard
layout: post
guid: https://jameshoward.us/?p=3325
permalink: /2015/12/09/numerical-analysis-talk-at-statistical-programming-dc/
dsq_thread_id:
  - "4388044602"
ampforwp_custom_content_editor_checkbox:
  - ""
featured-image: nair-840x500.png
categories:
  - Blog
tags:
  - CMNA
  - data science
  - mathematics
  - matlab
  - numerical analysis
  - R
  - scientific computing
  - talks
  - videos
---
I gave my talk tonight on numerical analysis in R and the talk is already up on YouTube.  

<iframe width="640" height="360" src="https://www.youtube-nocookie.com/embed/BmH9iZ-w4PQ?showinfo=0" frameborder="0" allowfullscreen></iframe>

There's an interesting set of questions at the end about resources for introducing new users to R.  The slides are not terribly visible, so you can see them here:

[slideshare id=55960098&doc=numericalanalysisinr-151209044934-lva1-app6892]

And this is the R script used for demonstrations:

[sourcecode language="R"]
## Example of vector arithmetic
u &lt;- c(1, 2, 3); v &lt;- c(8, 4, 2); x &lt;- 7
u + x
u + v

## Element recycling
u + c(1, 9)

## Matrix arithmetic
A &lt;- matrix(1:9, 3)
A + 1
A + u
A + c(1, 2)

## Diagonalization
(B &lt;- matrix(1:6, 3))
diag(A)
diag(B)

## Matrix multiplication
A %*% B

## Cross product 
crossprod(A, B)

## Outer product
outer(u, v)

## dot product
u %*% u 

## Matrix solution / RREF
(A &lt;- matrix(c(2, 3, 1, 1, 2, -5, -1, -2, 4), 3))
(b &lt;- c(1, 1, 3))
solve(A, b)

## LU Decomposition
library(Matrix)
lu(A)

## Linear interpolation
x &lt;- 1:10
y &lt;- log(x)
plot(x, y, main = &quot;approxfun demo&quot;)
par(new = TRUE)
flog &lt;- approxfun(x, y)
plot(flog, 1, 10, col = &quot;blue&quot;)

## Spline
x &lt;- seq(-10, 10, 4)
y &lt;- x^2 + 5 * x - 3
plot(x, y, main = &quot;splinefun demo&quot;)
par(new = TRUE)
linfun &lt;- approxfun(x, y)
plot(linfun, -10, 10, col = &quot;blue&quot;)
par(new = TRUE)
linfun &lt;- splinefun(x, y)
plot(linfun, -10, 10, col = &quot;green&quot;)

## Polynomial interpolation
polyinterp &lt;- function(x, y) {
  if(length(x) != length(y))
    stop(&quot;Length of x and y vectors must be the same&quot;)
  
  n &lt;- length(x) - 1
  vandermonde &lt;- rep(1, length(x))
  for(i in 1:n) {
    xi &lt;- x^i
    vandermonde &lt;- cbind(xi, vandermonde)
  }
  beta &lt;- solve(vandermonde, y)
  
  names(beta) &lt;- NULL
  return(rev(beta))
}

x &lt;- c(1, 2, 3)
y &lt;- x^2 + 5 * x - 3
z &lt;- polyinterp(x, y)

rhorner(1, z)

## Integration
integrate(log, 2, 6)
integrate(flog, 2, 6)

## Root Finding
## x^2 + x - 6
f &lt;- function(x) { (x + 3) * (x - 2) }             
plot(f, -5, 5, col = &quot;blue&quot;)
abline(h = 0, v = 0, col = &quot;black&quot;, lty = &quot;dotted&quot;) 
uniroot(f, c(-5, 0))

z &lt;- c(-6, 1, 1)
polyroot(z)

## x^2 + x + 6
z &lt;- c(6, 1, 1)
polyroot(z)

## Horner's method
rhorner &lt;- function(x, betas) {
  n &lt;- length(betas)
  
  if(n == 1)
    return(betas)
  
  return(betas[1] + x * rhorner(x, betas[2:n]))
}

rhorner(z, 5)
[/sourcecode]

Many thanks to [Marck Vaisman](https://about.me/marckvaisman) for putting this together and [Casey Patrick Driscoll](https://caseypatrickdriscoll.com/) for putting it on YouTube!
