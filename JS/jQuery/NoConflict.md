<a href="/JS/jQuery/AJAX.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/jQuery/Filters.md">Next &gt;</a>
<hr>
What if you wish to use other frameworks on your pages, while still using jQuery?
<h1>jQuery and Other JavaScript Frameworks</h1>
As you already know; jQuery uses the <code>$</code> sign as a shortcut for jQuery.
<br>
There are many other popular JavaScript frameworks like: Angular, Backbone, Ember, Knockout, and more.
<br><br>
<b>What if other JavaScript frameworks also use the</b> <code>$</code> <b>sign as a shortcut?</b>
<br>
If two different frameworks are using the same shortcut, one of them might stop working.
<br>
The jQuery team have already thought about this, and implemented the <b>noConflict()</b> method.
<h1>The noConflict() Method</h1>
The <b>noConflict()</b> method releases the hold on the $ shortcut identifier, so that other scripts can use it.
<br>
You can of course still use jQuery, simply by writing the full name instead of the shortcut:
<pre>
$.noConflict();
jQuery(document).ready(function(){
  jQuery("button").click(function(){
    jQuery("p").text("jQuery is still working!");
  });
});
</pre>
You can also create your own shortcut very easily. The <b>noConflict()</b> method returns a reference to jQuery, that you can save in a variable, for later use. Here is an example:
<pre>
var jq = $.noConflict();
jq(document).ready(function(){
  jq("button").click(function(){
    jq("p").text("jQuery is still working!");
  });
});
</pre>
If you have a block of jQuery code which uses the <code>$</code> shortcut and you do not want to change it all, you can pass the <code>$</code> sign in as a parameter to the ready method. This allows you to access jQuery using <code>$</code>, inside this function - outside of it, you will have to use "jQuery":
<pre>
$.noConflict();
jQuery(document).ready(function($){
  $("button").click(function(){
    $("p").text("jQuery is still working!");
  });
});
</pre>
