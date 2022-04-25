<a href="/JS/jQuery/Effects/Slide.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/jQuery/Effects/Stop.md">Next &gt;</a>
<hr>
With jQuery, you can create custom animations.
<h1>animate()</h1>
The jQuery <b>animate()</b> method is used to fade in a hidden element:
<pre>
$("button").click(function(){
  $("div").animate({left: "250px"});
});
</pre>
<b>Syntax:</b>
<pre>$(<i>selector</i>).animate(<i>speed</i>,<i>callback</i>);</pre>
<h1>Manipulate Multiple Properties</h1>
Notice that multiple properties can be animated at the same time:
<pre>
$("button").click(function(){
  $("div").animate({
    left: "250px",
    opacity: "0.5",
    height: "150px",
    width: "150px"
  });
});
</pre>
<h1>Using Relative Values</h1>
It is also possible to define relative values (the value is then relative to the element's current value). This is done by putting <code>+=</code> or <code>-=</code> in front of the value:
<pre>
$("button").click(function(){
  $("div").animate({
    left: "250px",
    height: "+=150px",
    width: "+=150px"
  });
});
</pre>
<h1>Using Pre-defined Values</h1>
You can even specify a property's animation value as "<b>show</b>", "<b>hide</b>", or "<b>toggle</b>":
<pre>
$("button").click(function(){
  $("div").animate({
    height: "toggle"
  });
});
</pre>
<h1>Uses Queue Functionality</h1>
By default, jQuery comes with queue functionality for animations.
<br>
This means that if you write multiple <b>animate()</b> calls after each other, jQuery creates an "internal" queue with these method calls. Then it runs the animate calls ONE by ONE.
<br>
So, if you want to perform different animations after each other, we take advantage of the queue functionality:
<pre>
$("button").click(function(){
  var div = $("div");
  div.animate({height: '300px', opacity: '0.4'}, "slow");
  div.animate({width: '300px', opacity: '0.8'}, "slow");
  div.animate({height: '100px', opacity: '0.4'}, "slow");
  div.animate({width: '100px', opacity: '0.8'}, "slow");
});
</pre>
The example below first moves the <b>&lt;div&gt;</b> element to the right, and then increases the font size of the text:
<pre>
$("button").click(function(){
  var div = $("div");
  div.animate({left: '100px'}, "slow");
  div.animate({fontSize: '3em'}, "slow");
});
</pre>
