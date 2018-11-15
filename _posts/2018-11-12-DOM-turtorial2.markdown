---
layout: post
title:  "Step 2 How to manipulate the DOM with javascript"
date:   2018-11-12 11:05:44 -0600
categories: Second post
author: "Marcus"
permalink: "/step2.html"
---

**In order for javascript to know where to apply the code you write you need to use one of the many selectors.**
I'll explain most of them below starting with the least interesting ones:

 Selector nr: 1 GETELEMENTBYID: This selector  uses the css id.
 {% highlight ruby %}
 /*you can store the location in a variable. In this case we store the ID 
 "header-title" in a varible of the same name but in camelCase*/
let headerTitle = document.getElementById('header-title')

/*if you then console.log the saved variable you will see 
the full tag in console.*/

console.log(headerTitle);

/*you can now manipulate the content within the ID. Here I add the text 'Hello' 
using textContent and then change it to 'Goodbye, with innerText, 
these two are very similar, but innerText will  get overwritten by style if you 
have a conflicting style in your html.  */
headerTitle.textContent = 'Hello';
headerTitle.innerText = 'Goodbye';

/*with innerHTML you can insert a tag and text.*/
headerTitle.innerHTML = '<h3>Hello</h3>';

/*you can also style your CSS in all possible ways*/
header.style.borderBottom = 'solid 3px #000';

/*note that we have to change the css syntax to camelCase, so Border-bottom
becomes borderBottom.*/
{% endhighlight %}
___

Selector nr: 2 GETELEMENTSBYCLASSNAME: this selector uses the css class name. It is especially
useful when there is more than one element on the page with the same class since it grabs all matching class names and present them in an array-like syntax.
 {% highlight ruby %}
 let items = document.getElementsbyClassName('Classname-of-list')

 /*shows an 0-based array of the list items*/
 console.log(items)

 /*shows the second li element*/
  console.log(items[1])

/*change the text in the first li element*/
items[0].textContent = 'Change me'

/*change text to bold on the third li element*/
items[2].style.fontWeight = 'bold'



{% endhighlight %}
___


Selector nr: 3 GETELEMENTSBYTAGNAME: this will grab all the tags of matching name on the page.
 {% highlight ruby %}
/* now all li's will be represented in an array-like syntax inside the
variable liElements*/
let liElements = document.getElementsbyTagName('li')

/*it will work as the getElementsbyClassName examples above*/

/*This is dangerous to use, if a new li element is inserted the array numbers
 will change. so use this with caution*/
{% endhighlight %}
___
**Here comes the good stuff, pay attention**

Selector nr: 4 QUERYSELECTOR: This is used only for one item, and will grab the first one if there is more than one. **You can use any css selector, class, ID, tag, list item.** 
 {% highlight ruby %}
 /*Grab the header by it's ID*/
let header = document.querySelector('#main-header')

/*insert a border at the bottom of header*/
header.style.borderBottom = 'solid 4px #f4f4f4'

/*if you have a bunch of list elements and want to grab any other than the 
first one you can use ":nth-child"*/

let firstItem = document.querySelector('.listofstuff')
firstItem.style.color = 'red'

/*note that nthchild is 1 based and not 0 based*/
let secondItem = document.querySelector('.listofstuff:nth-child(2)')
secondItem.style.color = 'blue'



 {% endhighlight %}
___

Selector nr: 5 QUERYSELECTORALL: Works similar to getElementsByTagName and ByClassName. It creates the array-like syntax but work on all kinds of tags, ids, classes, etc on the page. This is also better because it gets you a NodeList and we can run array functions on NodeLists!

{% highlight ruby %}
/* grab all <p> elements*/
let allPs = document.querySelectorAll('p')

/*Bold the third paragraph*/
allPs[2].style.fontWeight = 'bold'
{% endhighlight %}

[Step 3](/step3.html)

// Marcus 

<div
class="just-comments"
data-apikey="e3ae52cc-c19b-4c15-b6eb-2156879027b0">
</div>
<script async src="https://just-comments.com/w.js"></script>
