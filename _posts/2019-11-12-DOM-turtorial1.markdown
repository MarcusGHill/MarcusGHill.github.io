---
layout: post
title:  "Reflecting on  pre-compiling your css"
date:   2018-11-12 11:05:44 -0600
categories: Css
author: "Marcus"
permalink: "/precompiling.html"
---

**When you pre-compile your css you save alot of time and headace as a beginner**

**Compare to regular CSS**
in regular css as far as i know it is not possible to nest your tags like you can do with code. And this is kind of annoying. The ability to set variables in your css when you pre-compile is also a great timesaver and it makes it easier to always choose the same color whitout having to browse through you code every 5 seconds do crl:c + crl:v what ever random combination of #xxxxxx you happen to have as your color for h1´s.


**Which techniques did you use?**
Since I got a hard time making anything esthetic look good, weather it is digital or physical I used the minima theme as base for my site. I then looked at different free themes around the webb for insipiration and tried my best to make small changes to the main.css in order to reach my desired result. I got very surprised of how easy it was to manipulate the site and change it to my liking.


**Pros and cons?**
Someone as design handicaped as me could create a totaly acceptable site. I now feel like I can create basic, nice looking, simple sites in no time, something i thought impossible before this exercise.

**What is robots.txt and how have you configure it for your site?**
the Robots.txt file  is to give instructions to web robots or "web crawlers" usualy search engines, indexing the web. these instructions are called "the Robots Exclusion protocol. It is more of a finger pointer than instructions since the robots can fully disregard your Robots.txt file. I don´t want my site indext and searchable on google or other searchengines since it would be very confusing for people not taking my exact courses, and not having my specific knowledge to learn anything from my guides. Maybe one day i rewrite them in a general way but for now they are for me. Thats why my robots.txt file only has two lines: 
 {% highlight ruby %}
User-agent: *
Disallow: /
  {% endhighlight %}

  **What is humans.txt and how have you configure it for your site?**
  humans.txt is a textfile with information for knowing the people behind the site. The people who was a part in creating it. I have copied the standard provided at humanstxt.org. Since I'm the only creator and don´t use twitter or want a bunch of spam the information inmy humans.txt is not very useful in this case.

  **How did you implements comments to blog posts**
  The comments was a scary part that surprisingly just worked right away whitout any problems. I used "https://just-comments.com". Created a free account and pasted the code provided from them in my postlayout. It works great, code below.
   {% highlight ruby %}
<div
class="just-comments"
data-apikey="e3ae52cc-c19b-4c15-b6eb-2156879027b0">
</div>
<script async src="https://just-comments.com/w.js"></script>
  {% endhighlight %}

// Marcus 

<div
class="just-comments"
data-apikey="e3ae52cc-c19b-4c15-b6eb-2156879027b0">
</div>
<script async src="https://just-comments.com/w.js"></script>

