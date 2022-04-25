<a href="/JS/jQuery/Effects/.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/jQuery/Effects/.md">Next &gt;</a>
<hr>
<h1>Fade In</h1>
The jQuery <b>fadeIn()</b> method is used to fade in a hidden element:
<pre>
$("button").click(function(){
  $("#div1").fadeIn();
  $("#div2").fadeIn("slow");
  $("#div3").fadeIn(3000);
});
</pre>
<b>Syntax:</b>
<pre>$(<i>selector</i>).fadeIn(<i>speed</i>,<i>callback</i>);</pre>
<h1>Fade Out</h1>
The jQuery <b>fadeOut()</b> method is used to fade out a hidden element:
<pre>
$("button").click(function(){
  $("#div1").fadeOut();
  $("#div2").fadeOut("slow");
  $("#div3").fadeOut(3000);
});
</pre>
<b>Syntax:</b>
<pre>$(<i>selector</i>).fadeOut(<i>speed</i>,<i>callback</i>);</pre>
<h1>Fade Toggle</h1>
The jQuery <b>fadeToggle()</b> method toggles between the <b>fadeIn()</b> and <b>fadeOut()</b> methods.
<br>
If the elements are faded out, <b>fadeToggle()</b> will fade them in.
<br>
If the elements are faded in, <b>fadeToggle()</b> will fade them out.
<pre>
$("button").click(function(){
  $("#div1").fadeToggle();
  $("#div2").fadeToggle("slow");
  $("#div3").fadeToggle(3000);
});
</pre>
<b>Syntax:</b>
<pre>$(<i>selector</i>).fadeToggle(<i>speed</i>,<i>callback</i>);</pre>
<h1>Fade To</h1>
The jQuery <b>fadeTo()</b> method allows fading to a given opacity (value between 0 and 1):
<pre>
$("button").click(function(){
  $("#div1").fadeTo("slow", 0.15);
  $("#div2").fadeTo("slow", 0.4);
  $("#div3").fadeTo("slow", 0.7);
});
</pre>
<b>Syntax:</b>
<pre>$(<i>selector</i>).fadeTo(<i>speed</i>,<i>callback</i>);</pre>
