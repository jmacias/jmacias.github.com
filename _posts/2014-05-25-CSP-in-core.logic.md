---
layout: post
title: Solving a Constraint Satisfaction Problem with core.logic
published: true
---

A few days back a co-worker presented a puzzle. The puzzle was a Constraint Satisfaction Problem which I solved using [core.logic][core.logic]. Here is the puzzle description:

>In the picture below, find a solution by "configuring" each circle. Allowable configurations for each circle are the numbers 1 through 8. A couple of rules: 1) You cannot repeat any numbers, all numbers 1 through 8 must be used and 2) No two circles connected by arrows can have consecutive numbers (e.g. if the left most circle is a 4, then the circles to the right of it cannot be labeled a 3 or 5).

![problem](/static/images/CSPExample.jpg)

And here is the solution:

<script src="https://gist.github.com/jmacias/99d15323c6413c1c89a0.js"></script>

This was my first program using core.logic and it was really fun. 
 
[core.logic]: https://github.com/clojure/core.logic
