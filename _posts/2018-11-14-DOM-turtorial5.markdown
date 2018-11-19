---
layout: post
title:  "Step 5 eventListeners"
date:   2018-11-12 11:05:44 -0600
categories: fifth post
author: "Marcus"
permalink: "/step5.html"
---
Now it's time for eventListeners.

So in our HTLM we got this button
{% highlight ruby %}
<button id="button">Click Here</button>
 {% endhighlight %}

 ___

 we want to listen if the user clicks on it and execute a function if the button gets clicked
 inside the parenthesis of eventListener the first parameter is what event to listen for and the second is what to do if that event is detected.
 in this case, run the function "youClicked".
 {% highlight ruby %}
let buttonClicked = document.querySelector(#button).eventListener('click', youClicked)

function youClicked(){
    /*code for what you want to happen when button is clicked*/¨
  console.log('you clicked my button')
}
 {% endhighlight %}
 ___

Adding event parameter. The name can be whatever but is usualy event or e.
{% highlight ruby %}
function youClicked(e){
    /*will give us the full button tag declared above*/
console.log(e.target)

/*returns button witch is the id of the button*/
console.log(e.target.id)

/*returns whatever type of event is being listened for in this case click*/
console.log(e.type)

/*find postion of the mouse, x and y axis, relative to the window*/
console.log(e.clientX)
console.log(e.clientY)

/*find postion of the mouse, x and y axis, relative to the object getting clicked, in this case button*/
console.log(e.offsetX)
console.log(e.offsetY)

/*findout if spedific key is held down while click, returns true if it is and false if it's not*/
console.log(e.altKey)
console.log(e.shiftKey)
console.log(e.ctrlKey)

}
 {% endhighlight %}

 All avaliable events you can listen for
{% highlight ruby %}
 Resource EventsSection
Event Name.  	Fired When.

cached	The resources listed in the manifest have been downloaded, and the application is now cached.
error	A resource failed to load.
abort	The loading of a resource has been aborted.
load	A resource and its dependent resources have finished loading.
beforeunload	The window, the document and its resources are about to be unloaded.
unload	The document or a dependent resource is being unloaded.
online	The browser has gained access to the network.
offline	The browser has lost access to the network.
focus	An element has received focus (does not bubble).
blur	An element has lost focus (does not bubble).
open	A WebSocket connection has been established.
message	A message is received through a WebSocket.
error	A WebSocket connection has been closed with prejudice (some data couldn't be sent for example).
close	A WebSocket connection has been closed.
pagehide	A session history entry is being traversed from.
pageshow	A session history entry is being traversed to.
popstate	A session history entry is being navigated to (in certain cases).
animationstart	A CSS animation has started.
animationend	A CSS animation has completed.
animationiteration	A CSS animation is repeated.
transitionstart	A CSS transition has actually started (fired after any delay).
transitioncancel	A CSS transition has been cancelled.
transitionend	A CSS transition has completed.
transitionrun	A CSS transition has begun running (fired before any delay starts).
reset	The reset button is pressed
submit	The submit button is pressed
beforeprint	The print dialog is opened
afterprint	The print dialog is closed
compositionstart	The composition of a passage of text is prepared (similar to keydown for a keyboard input, but works with other inputs such as speech recognition).
compositionupdate	A character is added to a passage of text being composed.
compositionend	The composition of a passage of text has been completed or canceled.
fullscreenchange	An element was turned to fullscreen mode or back to normal mode.
fullscreenerror	It was impossible to switch to fullscreen mode for technical reasons or because the permission was denied.
resize	The document view has been resized.
scroll	The document view or an element has been scrolled.
cut	The selection has been cut and copied to the clipboard
copy	The selection has been copied to the clipboard
paste	The item from the clipboard has been pasted
keydown	ANY key is pressed
keypress	ANY key except Shift, Fn, CapsLock is in pressed position. (Fired continously.)
keyup	ANY key is released
mouseenter	A pointing device is moved onto the element that has the listener attached.
mouseover	A pointing device is moved onto the element that has the listener attached or onto one of its children.
mousemove	A pointing device is moved over an element. (Fired continously as the mouse moves.)
mousedown	A pointing device button is pressed on an element.
mouseup	A pointing device button is released over an element.
auxclick	A pointing device button (ANY non-primary button) has been pressed and released on an element.
click	A pointing device button (ANY button; soon to be primary button only) has been pressed and released on an element.
dblclick	A pointing device button is clicked twice on an element.
contextmenu	The right button of the mouse is clicked (before the context menu is displayed).
wheel	A wheel button of a pointing device is rotated in any direction.
mouseleave	A pointing device is moved off the element that has the listener attached.
mouseout	A pointing device is moved off the element that has the listener attached or off one of its children.
select	Some text is being selected.
pointerlockchange	The pointer was locked or released.
pointerlockerror	It was impossible to lock the pointer for technical reasons or because the permission was denied.
dragstart	The user starts dragging an element or text selection.
drag	An element or text selection is being dragged (Fired continuously every 350ms).
dragend	A drag operation is being ended (by releasing a mouse button or hitting the escape key).
dragenter	A dragged element or text selection enters a valid drop target.
dragover	An element or text selection is being dragged over a valid drop target. (Fired continuously every 350ms.)
dragleave	A dragged element or text selection leaves a valid drop target.
drop	An element is dropped on a valid drop target.
durationchange	The duration attribute has been updated.
loadedmetadata	The metadata has been loaded.
loadeddata	The first frame of the media has finished loading.
canplay	The browser can play the media, but estimates that not enough data has been loaded to play the media up to its end without having to stop for further buffering of content.
canplaythrough	The browser estimates it can play the media up to its end without stopping for content buffering.
ended	Playback has stopped because the end of the media was reached.
emptied	The media has become empty; for example, this event is sent if the media has already been loaded (or partially loaded), and the load() method is called to reload it.
stalled	The user agent is trying to fetch media data, but data is unexpectedly not forthcoming.
suspend	Media data loading has been suspended.
play	Playback has begun.
playing	Playback is ready to start after having been paused or delayed due to lack of data.
pause	Playback has been paused.
waiting	Playback has stopped because of a temporary lack of data.
seeking	A seek operation began.
seeked	A seek operation completed.
ratechange	The playback rate has changed.
timeupdate	The time indicated by the currentTime attribute has been updated.
volumechange	The volume has changed.
complete	The rendering of an OfflineAudioContext is terminated.
audioprocess	The input buffer of a ScriptProcessorNode is ready to be processed.
loadstart	Progress has begun.
progress	In progress.
error	Progression has failed. 
timeout	Progression is terminated due to preset time expiring.
abort	Progression has been terminated (not due to an error).
load	Progression has been successful.
loadend	Progress has stopped (after "error", "abort" or "load" have been dispatched).
change (see Non-standard events)
storage

{% endhighlight %}
<div class="share-page">
  Share this on &rarr;
  <a href="https://twitter.com/intent/tweet?text={{ page.title }}&url={{ site.url }}{{ page.url }}&via={{ site.twitter_username }}&related={{ site.twitter_username }}" rel="nofollow" target="_blank" title="Share on Twitter">Twitter</a>
</div> 
<div
class="just-comments"
data-apikey="e3ae52cc-c19b-4c15-b6eb-2156879027b0">
</div>
<script async src="https://just-comments.com/w.js"></script>