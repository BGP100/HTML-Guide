<a href="/JS/DOM/CSS.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/DOM/Events.md">Next &gt;</a>
<hr>
Learn to create HTML animations using JavaScript.
<h1>Create an Animation Container</h1>
All animations should be relative to a container element.
<pre>
&lt;div id="container"&gt;
  &lt;div id="animate"&gt;My animation will go here&lt;/div&gt;
&lt;/div&gt;
</pre>
<h1>Style the Elements</h1>
The container element should be created with style = "position: relative".
<br>
The animation element should be created with style = "position: absolute".
<pre>
#container {
  width: 400px;
  height: 400px;
  position: relative;
  background: yellow;
}
#animate {
  width: 50px;
  height: 50px;
  position: absolute;
  background: red;
}
</pre>
<h1>Animation Code</h1>
JavaScript animations are done by programming gradual changes in an element's style.
<br>
The changes are called by a timer. When the timer interval is small, the animation looks continuous.
<br>
The basic code is:
<pre>
id = setInterval(frame, 5);
function frame() {
  if (/* test for finished */) {
    clearInterval(id);
  } else {
    /* code to change the element style */ 
  }
}
</pre>
<h1>Create the Full Animation Using JavaScript</h1>
<pre>
function myMove() {
  let id = null;
  const elem = document.getElementById("animate");
  let pos = 0;
  clearInterval(id);
  id = setInterval(frame, 5);
  function frame() {
    if (pos == 350) {
      clearInterval(id);
    } else {
      pos++;
      elem.style.top = pos + 'px';
      elem.style.left = pos + 'px';
    }
  }
}
</pre>
