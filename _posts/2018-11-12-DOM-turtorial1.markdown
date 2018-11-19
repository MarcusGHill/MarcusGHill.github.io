---
layout: post
title:  "Step 1 What is the DOM?"
date:   2018-11-12 11:05:44 -0600
categories: First post
author: "Marcus"
permalink: "/step1.html"
---
adding this test
**In my experience the best way to learn is to try to teach others**
that's why this blog will be dedicated to teching the DOM, javascript, HTML CSS and how to manipulate the DOM with javascript.
This blog will be a short turtorial to DOM and javascript and what you need to know to manipulate the DOM with javascript.

I will assume that you already have basic knowledge of Javascript, HTML and css. 

DOM is short for DOCUMENT OBJECT MODEL. The DOM is a tree of nodes/Elements created in HTML by the browser. Javascript can be used to read/write and manipulate the DOM. 

if a element nests inside another element it is considered a child of the element it nests inside of. example:

{% highlight ruby %}
<div id="parent">  
 <p> this is child  </p>  
 </div> 
{% endhighlight %}

the id is not important to the child/parent relationship, it´s only there in this case to point out that the div is the parent to the p.

___

First of all we'll need to link our javascript code to our HTML page. We do this by adding the following code right before our closing head tag.
**(for modern browsers)**, Old bowsers will skip this.

{% highlight ruby %}
/* in this case the app.js file is stored in the js folder. */
<script type="module" src="js/app.js"></script>
{% endhighlight %}

In order to get some back compability we add  the nomodule script tag right before the closing body tag  **(for old browsers)**, modern bowsers will skip this.
This works if you got webbpack installed as webbpack rebuilds your code to match older bowsers compability.
{% highlight ruby %}
<script nomodule src="build.js"></script>
{% endhighlight %}

Check my next post for information of how to use javascript to manipulate the DOM.

[Step 2](/step2.html)

// Marcus 
<div class="share-page">
  Share this on &rarr;
  <a href="https://twitter.com/intent/tweet?text={{ page.title }}&url={{ site.url }}{{ page.url }}&via={{ site.twitter_username }}&related={{ site.twitter_username }}" rel="nofollow" target="_blank" title="Share on Twitter">Twitter</a>
</div>
<div
class="just-comments"
data-apikey="e3ae52cc-c19b-4c15-b6eb-2156879027b0">
</div>
<script async src="https://just-comments.com/w.js"></script> 
