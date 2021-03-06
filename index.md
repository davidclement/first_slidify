---
title       : Exploring Bayes Law and Medical Testing
subtitle    : 
author      : David Clement
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax,bootstrap]  # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Developing an Intution for Bayes Law

In the statistical inference class, I became curious about
Bayes Law in the context of medical testing.  I wanted to understand
it in a more visual, intuitive way, like the way a 50/50 coin flip 
can be represented simply as two equal, non-overlapping areas:

<img src="assets/fig/unnamed-chunk-1-1.png" title="plot of chunk unnamed-chunk-1" alt="plot of chunk unnamed-chunk-1" style="display: block; margin: auto;" />
Could the interpretation of a medical test given Prevalence, Specificity, and Sensitivity be represented in the same terms?

--- .class #id

## Bayes' Law as a Formula

At least for me, the expression and derivation of Bayes' Law in symbols was less intuitive than the pictures representing simple probabilities.  I wondered if that was due to the inherent abstractness of the concept.  It certainly seemed to produce surprising results, as when a positive test for a rare disease might, more often than not, be wrong -- even when the test had high sensitivity and specificity.  

Bayes' Law as a formula: 

$$P(B|A) = \frac{P(A|B) P(B)}{P(A|B) P(B) + P(A|B^c)(P(B^c)}$$

--- .class #id 

## A Visual Representation of Bayes Law

I wasn't able to find a visual interpretation of the conditional 
probability involved in medical testing similar to the simple box divided into two for heads and tails. 

### The question: What would such a visualization look like?

My Shiny App is an attempt to answer that question, and it comes from a realization that the same simple approach of using areas to represent probabilities works with the more complicated conditional probability.


--- .class #id 


## The App

Here's the app. [Exploring Bayes Law and Medical Testing](https://davidclement.shinyapps.io/Project)

It allows you to explore visually, the influence of three parameters
- **Prevalence**: the chance that a person has a disease of interest
- **Sensitivity**: the chance that the test for the disease will correctly detect the disease in a person who has it.
- **Specificity**: the chance that the test for the disease will correctly find that a person doesn't have it, when they truly don't.


