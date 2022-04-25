<a href="/JS/jQuery/Effects/Stop.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/jQuery/Effects/Chaining.md">Next &gt;</a>
<hr>
<h1>Functions</h1>
JavaScript statements are executed line by line. However, with effects, the next line of code can be run even though the effect is not finished. This can create errors.
<br>
To prevent this, you can create a callback function.
<br>
A callback function is executed after the current effect is finished.
<br><br>
The example below has a callback parameter that is a function that will be executed after the hide effect is completed:
<pre>
$("button").click(function(){
  $("p").hide("slow", function(){
    alert("The paragraph is now hidden");
  });
});
</pre>
The example below has no callback parameter, and the alert box will be displayed before the hide effect is completed:
<pre>
$("button").click(function(){
  $("p").hide(1000);
  alert("The paragraph is now hidden");
});
</pre>
<b>Typical syntax:</b> <code>$(<i>selector</i>).hide(<i>speed</i>,<i>callback</i>);</code>
