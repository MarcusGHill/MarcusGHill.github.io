---
layout: post
title:  "Step 2 How to manipulate the DOM with javascript"
date:   2018-11-12 11:05:44 -0600
categories: Second post
author: "Marcus"
permalink: "/step2"
---

In order for javascript to know where to apply the code you write you need to use one of the many selectors. 
I'll explain most of them below:

 GETELEMENTBYID: This method  uses the css id to find out where on the page you are telling it to do something.
 {% highlight ruby %}
 /*you can store the location in a variable. In this case we store the ID 
 "header-title" in a varible of the same name.*/
let headerTitle = document.getElementById('header-title')

/*if you then console.log the saved variable you will see 
the full tag in console.*/

console.log(headerTitle);

/*you can now manipulate the content within the ID. Here I add the text 'Hello' using textContent
 and then change it to 'Goodbye, with innerText, these two are very similar but innerText
 will  get overwritten by style if you have a conflicting style in your html.  */
headerTitle.textContent = 'Hello';
headerTitle.innerText = 'Goodbye';

/*with innerHTML you can insert a tag and text.*/
headerTitle.innerHTML = '<h3>Hello</h3>';

/*you can also style your CSS in all possible ways
header.style.borderBottom = 'solid 3px #000';
{% endhighlight %}

[Step 3](/step3.html)

// Marcus 

<div
class="just-comments"
data-apikey="e3ae52cc-c19b-4c15-b6eb-2156879027b0">
</div>
<script async src="https://just-comments.com/w.js"></script>