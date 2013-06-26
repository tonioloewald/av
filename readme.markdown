How to use HTML5 <video> and <audio> tags everywhere 
===========================

(and have them Just Work&trade;)
---------------------------

<video src="media/walk.m4v" width="480" height="270" loop="true" autoplay="true" controls="true">


Audio embedded in a video tag
-----------------------------

<video src="media/ratchet.mp3" width="240" height="16" loop="true" autoplay="false" controls="true">

Note that the above isn't supposed to work, but does work in Safari (and may work in other browsers) and also works with my av.swf media player.

Audio embedded in an audio tag
------------------------------

<audio src="media/speeder.mp3" width="240" height="16" loop="true" autoplay="false" controls="true">

Click <button onclick=""av.replace_html5_media_tags();">Test Flash Switch</button> to swap in the Flash player for all <audio> and <video> elements (this lets me test it all works without launching a crippled web browser).

Notes
-----

* I've chosen to make my player controls minimal in the spirit of Apple's HTML5 video player UI. Why? Because I kind of agree with Apple that the system volume control is the volume control.

* Because I couldn't figure out how to "puppet" Flash's video control components, all the UI elements are implemented from scratch. (Not a huge deal and much easier to customize.)
To Do

It might be helpful to "package" this up a little better so that, for example, it works regardless of where the web page is relative to the flash player. Any coder should be able to tweak the code to work properly for his/her site as is but it's not quite a no-brainer.
Expose all the relevant routines in the flash player (they're already factored with this in mind so it's not going to be much work).

Write some abstraction routines into av.js for talking to the videos as if they were video tags. Ideally I'd replicate the html5 video API for Flash but I've not done that kind of thing before and I don't know how hairy it is (Google's excanvas.js does exactly this kind of thing so maybe I can find clues there).

W.r.t. the above, I'd like to be able to use the Flash player (if only for test purposes) even if it's not needed, which may make the previous item harder. I guess it's better to expose a constant API than be able to perform this kind of dirty trick.

There's more information in the two blog posts I wrote about this "How to use HTML5 &lt;video&gt; tags everywhere and have them Just Work&trade;" and "How to use HTML5 Video and Audio Tags Everywhere". If you have comments, questions, or suggestions please contact me at tonio at loewald dot com.

<script src="jquery.js"></script>
<script src="av.js"></script>
