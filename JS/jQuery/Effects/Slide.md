<a href="/JS/jQuery/Effects/Fade.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/jQuery/Effects/Animate.md">Next &gt;</a>
<hr>
<h1>Slide Down</h1>
The jQuery <b>slideDown()</b> method is used to slide up an element:
<pre>
$("#flip").click(function(){
  $("#panel").slideDown();
});
</pre>
<b>Syntax:</b>
<pre>$(<i>selector</i>).slideDown(<i>speed</i>,<i>callback</i>);</pre>
<h1>Slide Up</h1>
The jQuery <b>slideUp()</b> method is used to slide up an element:
<pre>
$("#flip").click(function(){
  $("#panel").slideUp();
});
</pre>
<b>Syntax:</b>
<pre>$(<i>selector</i>).slideUp(<i>speed</i>,<i>callback</i>);</pre>
<h1>Slide Toggle</h1>
The jQuery <b>slideToggle()</b> method toggles between the <b>slideDown()</b> and <b>slideUp()</b> methods.
<br>
If the elements are slided out, <b>slideToggle()</b> will fade them in.
<br>
If the elements are slided in, <b>slideToggle()</b> will fade them out.
<pre>
$("#flip").click(function(){
  $("#panel").slideToggle();
});
</pre>
<b>Syntax:</b>
<pre>$(<i>selector</i>).slideToggle(<i>speed</i>,<i>callback</i>);</pre>
