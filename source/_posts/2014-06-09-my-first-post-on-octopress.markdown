---
layout: post
title: "My Zeroth Post"
date: 2014-06-10 10:42:32 -0400
comments: true
categories: Flatiron&nbsp;School Edsger&nbsp;Dijkstra Indexing Zero-based&nbsp;numbering
---
Thanks for stumbling across my zeroth post on my very zeroth blog. Why zeroth? We'll get to that in just a little bit.
<!--more-->
Since starting the RUBY-005 class at Flatiron School, we've been beginning lecture by focusing on a different programmer each day and discussing their contributions to computing. My favorite so far has definitely been <a href="http://en.wikipedia.org/wiki/Edsger_Dijkstra" target="_blank">Edsger Dijkstra</a>. Besides him being the father of structured programming (something I am immensely grateful for), I found his sense of humor to be incredibly refreshing. Here are a couple of my favorite quotes of his below:

<em>"About the use of language: it is impossible to sharpen a pencil with a blunt axe. It is equally vain to try to do it with ten blunt axes instead."</em>

<em>"It is practically impossible to teach good programming to students that have had a prior exposure to BASIC: as potential programmers they are mentally mutilated beyond hope of regeneration."</em>

Wow, harsh. Pretty much the entirety of my experience with BASIC centered around playing the QBasic game <a href="http://en.wikipedia.org/wiki/Gorillas_(video_game)" target="_blank">Gorillas</a> when I was in elementary school. That statement alone makes me happy I never took my curiousity further than that.

One of the first hang-ups I had as a coding beginner was the concept of zero-based numbering; that the first element in a given array has an index of 0, not 1. It was really more of a minor annoyance than anything else - everything I had encountered up until this point began with a count of 1, and the habit of thinking in that manner found me making the same mistakes in my code over and over again.

Dijkstra argued in favor of zero-based numbering in a <a href="http://www.cs.utexas.edu/users/EWD/transcriptions/EWD08xx/EWD831.html" target="_blank">paper</a> he wrote while at the University of Texas. I still can't say I completely agree with the use of it semantically, but it was very interesting to gain a new perspective on how it makes sense from a mathematical standpoint.

His argument centers around the idea that expressing the range of a<br> variable <strong>i</strong> as <strong>x <= i < y</strong> offers advantages over any other combination of inequalities. Besides his belief that zero is the smallest natural number, I found the following reasons to be the most compelling for its usage:

&bull; In some tasks it's useful to ask <em>"How many values occured <strong>i</strong> times?</em>" Placing such values in an array requires beginning the indices at 0; in the case one has the possibility that some values occurred zero times.

&bull; Consecutive ranges have matching end-points:
<strong>x <= i < y</strong> followed by <strong>y <= i < z</strong> yields <strong>x <= i < z</strong>.

&bull; The length of the range is the difference of its endpoints:
<strong>0 <= i < 10</strong> has ten elements, as does <strong>5 <= i < 15</strong>.

&bull; In iterative algorithms that count from zero, the current
value of the count always equals the number of previous
iterations.

&bull; For a zero-origin array, the index indicates the
displacement from the origin.

I believe that the language should adapt to the user when at all possible, not the other way around. However, Dijkstra makes a lot of points that are very difficult to counter. At least for my decidedly un-mathy brain.







