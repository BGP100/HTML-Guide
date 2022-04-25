<a href="/JS/jQuery/Effects/Animate.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/jQuery/Effects/Callback.md">Next &gt;</a>
<hr>
The jQuery <b>stop()</b> method is used to stop animations or effects before it is finished.
<h1>The stop() Method</h1>
The jQuery <b>stop()</b> method is used to stop an animation or effect before it is finished.
<br>
The <b>stop()</b> method works for all jQuery effect functions, including sliding, fading and custom animations.
<pre>
$("#stop").click(function(){
  $("#panel").stop();
});
</pre>
<b>Syntax:</b>
<pre>$(<i>selector</i>).stop(<i>stopAll</i>,<i>goToEnd</i>);</pre>
