---
layout: post
title:  "Step 3 Navigation around the DOM"
date:   2018-11-12 11:05:44 -0600
categories: Third post
author: "Marcus"
permalink: "/step3"
---


**When we got our selectors down we are going to start navigation around the DOM.**
below is a quick explanation of the parent/sibling/child structure of the DOM.

 {% highlight ruby %}
<div class="imTheParentHere">  /* The div is the parent, since the other elements
 are nested inside it, these elements are the children of this div*/
<p class="myP"><p> /*The p is a child to div and a sibling to h2 and ul since they 
are nested inside the same div*/
<h2><h2> /*the h2 is a child to div and sibling to p and ul*/
<ul id =items> /*li is children of ul, ul is child of div and sibling to h2 & p*/
<li><li>
<li><li>
<li><li>
<li><li>
<li><li>
<ul>
 <div> /*end of parent*/
 {% endhighlight %}

So let's se how we use parents and children to select specific elements.

 {% highlight ruby %}
 /*First we grab the ul by it's ID*/
let itemList =  document.querySelector('#items')

/*grab parent of ul and put it in a variable */
let parent = itemList.parentNode

/*now you can change whatever you want of the div, example*/
parent.style.backgroundColor = '#f4f4f4'

/*we can chain this and extend it as far as we want 
(until there is no more parent).*/
let greatGrandParent = parent.parentNode.parentNode

/*instead of parentNode we could use parentElement and these two are for the 
most part interchangable*/

/* Now same thing with ChildNodes, using the same variable created above,  "itemList"*/
let liElements = itemList.childNodes
/*this will how ever not only grab the 5 li elements and but them in an 
nodelist it will also grab all the linebreaks and assign them to every 
other position in the nodelist. This is kind of a pain in the ass so i suggest
you don't use child nodes, instead use children*/

/*children instead of childNodes, I overwrite the same variable. This returns
a HTMLCollection instead of nodelist but it works almost the same */
liElements = itemList.children
/*changes the third li elements background color*/
liElements[2].style.backgroundColor = 'red'  


/*firstElementChild & lastElementChild this will grab the first or the last li element*/
let firstLi = itemList.firstElementChild
firstLi.textContent = 'Text inside the first li'
let lastLi = itemList.lastElementChild
lastLi.textContent = 'Text inside the last li'
{% endhighlight %}

Now lets have a look at siblings, using the same DOM-tree and variable as above.
 {% highlight ruby %}
 /*nextSibling, just like childNodes return line breaks as elements so the 
 variable sibling below would contain a empty #text, and the the ul element in our tree
 does not have a next sibling so it would return null where it not for the line break*/
let sibling = itemList.nextSibling

/*let't chose a example that will return a sibling and not give us a line break as a 
empty textNode*/
sibling = document.querySelector('.myP')

/*this will select the next sibling to the p element witch is the h2, 
and since we use the nextElementSibling we don't have to deal 
with the empty textNodes*/
let nextSibling = sibling.nextElementSibling 


/*previousSibling, this return the textNode so I wont even bother */

/*PreviousElementSibling, This is what we want to use and it works like 
nextElementSibling but in opposit direction*/
let thisWillBeTheH2 = itemList.previousElementSibling
thisWillBeTheH2.style.color = 'red'
 {% endhighlight %}
[Step 4](/step4.html)

<div
class="just-comments"
data-apikey="e3ae52cc-c19b-4c15-b6eb-2156879027b0">
</div>
<script async src="https://just-comments.com/w.js"></script>
