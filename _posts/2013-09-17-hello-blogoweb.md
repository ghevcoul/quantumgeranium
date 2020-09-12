---
layout: post
title: Hello Blogoweb!
author: Gavin
slug: hello-blogoweb
---

Greetings fine people of the internet and welcome to my little corner
of it.
<!--more-->

I intend to use this space to discuss my research and any other science
I find interesting, although I expect that it will be interspersed with
other topics I feel compelled to discuss.

In recent news, after one year of work and a bunch of iterations the
model that I am developing and testing with my postdoc supervisor is
finally producing results that match with the established ways of
calculating these things.

{% figure caption:"Blue dots show results from traditional way of doing things and the red
line shows the results from our model." %}
![A vague graph](/assets/VagueGraph-Sept17.png)
{% endfigure %}

As you can see in the unlabeled graph above, the model and traditional
way of doing things produce curves with the same slope, but offset
y-intercepts (we are currently working on fixing that). Note that I am
being deliberately vague here because this work is currently unpublished
and I can't say too much until after it is.

Over 6000 hours of CPU time (a bit more than 250 days) went into
acquiring all the data that went into the blue curve. The red curve, on
the other hand, simply used 9 hours of CPU time.  Even if we can't get
the y-intercept issue sorted out, there is still usefulness in being
able to get some predictive data in 0.15% of the time.
