---
layout: post
title:  "Step 4 Creating HTML elements with javascript"
date:   2018-11-12 11:05:44 -0600
categories: forth post
author: "Marcus"
permalink: "/step4.html"
---

**Now lets learn how to create elements in the DOM through javascript**
 {% highlight ruby %}
 /*Creates a new empty div, both opening and closing tags*/
 let newDiv = document.createElement('div')

 /*add class to this  Div element*/
 newDiv.className = 'className'

 /*add id*/
 newDiw.id = 'idName'

/* Give the div an attribute. The first parameter inside the setAttrubute () 
is the attribute you want, in this case title, the second parameter is the name of
 this attribute. (more on attributes */
newDiv.setAttribute('title', 'nameOfTitle')

/* attributes are HTML. some of the most common are: alt, disabled, href, id, src, 
style,title*/


/*So now we only have an empty div element with class, id and title but no text content. 
First we create a textNode with the text*/
let newDivText = document.createTextNode('the text we want to insert')

/*Add the textNode to the div. textNodes are paragraphs. And we want this paragraph 
to be nested inside the div. thus we want it to be a child of the div*/
newDiv.appendChild(newDivText)

/*Now the text is inserted inside the div but its not yet in the DOM. We now need to 
decide where in the DOM we want to put this new div with it's content. First we'll 
grab a location from the DOM represented below */

  <header id="main-header">
 "we want to place our div right here"
    <div class="container">
      <h1 id="header-title">Item Lister <span style="display:none">123</span></h1>
    </div>
  </header>


/*create a variable for the block where we want to insert our div*/
let whereToInsert = document.querySelector('.container')

/*create a variable for the positon inside the block after where we want our div. 
we need to be specific and type (header h1) meaning the h1 in the header. */
let positionAfterIsH1 = document.querySelector('header h1')

/*Insert our div in the container block before the h1. insertBefore is a method, 
syntax is parentNode.insertBefore(elementToInsert, positionAfter)*/
whereToInsert.insertBefore(newDiv, positionAfterIsH1)

/*now you can manipulate this just as before*/
newDiv.style.color = 'red'
newDiv.style.fontSize = '50px'
  {% endhighlight %}

[Step 5](/step5.html)

<div
class="just-comments"
data-apikey="e3ae52cc-c19b-4c15-b6eb-2156879027b0">
</div>
<script async src="https://just-comments.com/w.js"></script>
<script src="assets/app.js"></script>