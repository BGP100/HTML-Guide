<a href="/CSS/Advanced/Transtions.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Advanced/Tooltip.md">Next &gt;</a>
<hr>
CSS allows animation of HTML elements without using JavaScript or Flash!
<br>
<img src="https://i.imgur.com/C4ESWXb.gif" width="80%">
<br>
In this chapter you will learn about the following properties:
<ul>
  <li><b>@keyframes</b></li>
  <li><b>animation-name</b></li>
  <li><b>animation-duration</b></li>
  <li><b>animation-delay</b></li>
  <li><b>animation-iteration-count</b></li>
  <li><b>animation-direction</b></li>
  <li><b>animation-timing-function</b></li>
  <li><b>animation-fill-mode</b></li>
  <li><b>animation</b></li>
</ul>
<h1>Browser Support</h1>
The numbers in the table specify the first browser version that fully supports the property.
<table class="ws-table-all">
  <tr>
    <th>Property</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>@keyframes</td>
    <td>43.0</td>
    <td>10.0</td>
    <td>16.0</td>
    <td>9.0</td>
    <td>30.0</td>
  </tr>
  <tr>
    <td>animation-name</td>
    <td>43.0</td>
    <td>10.0</td>
    <td>16.0</td>
    <td>9.0</td>
    <td>30.0</td>
  </tr>
  <tr>
    <td>animation-duration</td>
    <td>43.0</td>
    <td>10.0</td>
    <td>16.0</td>
    <td>9.0</td>
    <td>30.0</td>
  </tr>
  <tr>
    <td>animation-delay</td>
    <td>43.0</td>
    <td>10.0</td>
    <td>16.0</td>
    <td>9.0</td>
    <td>30.0</td>
  </tr>
  <tr>
    <td>animation-iteration-count</td>
    <td>43.0</td>
    <td>10.0</td>
    <td>16.0</td>
    <td>9.0</td>
    <td>30.0</td>
  </tr>
  <tr>
    <td>animation-direction</td>
    <td>43.0</td>
    <td>10.0</td>
    <td>16.0</td>
    <td>9.0</td>
    <td>30.0</td>
  </tr>
  <tr>
    <td>animation-timing-function</td>
    <td>43.0</td>
    <td>10.0</td>
    <td>16.0</td>
    <td>9.0</td>
    <td>30.0</td>
  </tr>
  <tr>
    <td>animation-fill-mode</td>
    <td>43.0</td>
    <td>10.0</td>
    <td>16.0</td>
    <td>9.0</td>
    <td>30.0</td>
  </tr>
  <tr>
    <td>animation</td>
    <td>43.0</td>
    <td>10.0</td>
    <td>16.0</td>
    <td>9.0</td>
    <td>30.0</td>
  </tr>
</table>
<h1>What are Animations?</h1>
An animation lets an element gradually change from one style to another.
<br>
You can change as many CSS properties you want, as many times as you want.
<br>
To use CSS animation, you must first specify some keyframes for the animation.
<br>
Keyframes hold what styles the element will have at certain times.
<h1>@keyframe</h1>
When you specify CSS styles inside the <b>@keyframes</b> rule, the animation will gradually change from the current style to the new style at certain times.
<br>
To get an animation to work, you must bind the animation to an element.
<br>
The following example binds the "example" animation to the <b>&lt;div&gt;</b> element. The animation will last for 4 seconds, and it will gradually change the background-color of the <b>&lt;div&gt;</b> element from "red" to "yellow":
<pre>
/* The animation code */
@keyframes example {
  from {background-color: red;}
  to {background-color: yellow;}
}
/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
}
</pre>
<b><i>Note:</i></b> The animation-duration property defines how long an animation should take to complete. If the <b>animation-duration</b> property is not specified, no animation will occur, because the default value is 0s (0 seconds). 
<br>
In the example above we have specified when the style will change by using the keywords "from" and "to" (which represents 0% (start) and 100% (complete)).
<br>
It is also possible to use percent. By using percent, you can add as many style changes as you like.
<br>
The following example will change the background-color of the <b>&lt;div&gt;</b> element when the animation is 25% complete, 50% complete, and again when the animation is 100% complete:
<pre>
/* The animation code */
@keyframes example {
  0%   {background-color: red;}
  25%  {background-color: yellow;}
  50%  {background-color: blue;}
  100% {background-color: green;}
}
/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
}
</pre>
The following example will change both the background-color and the position of the <b>&lt;div&gt;</b> element when the animation is 25% complete, 50% complete, and again when the animation is 100% complete:
<pre>
/* The animation code */
@keyframes example {
  0% {background-color:red; left:0px; top:0px;}
  25% {background-color:yellow; left:200px; top:0px;}
  50% {background-color:blue; left:200px; top:200px;}
  75% {background-color:green; left:0px; top:200px;}
  100% {background-color:red; left:0px; top:0px;}
}
/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
}
</pre>
<h1>Delay</h1>
The <b>animation-delay</b> property specifies a delay for the start of an animation.
<br>
The following example has a 2 seconds delay before starting the animation:
<pre>
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-delay: 2s;
}
</pre>
Negative values are also allowed. If using negative values, the animation will start as if it had already been playing for <i>N</i> seconds.
<br>
In the following example, the animation will start as if it had already been playing for 2 seconds:
<pre>
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-delay: -2s;
}
</pre>
<h1>Set How Many Times an Animation Should Run</h1>
The <b>animation-iteration-count</b> property specifies the number of times an animation should run.
<br>
The following example will run the animation 3 times before it stops:
<pre>
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: 3;
}
</pre>
The following example uses the value "infinite" to make the animation continue for ever:
<pre>
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: infinite;
}
</pre>
<h1>Run in Reverse</h1>
The <b>animation-direction</b> property specifies whether an animation should be played forwards, backwards or in alternate cycles.
<br>
The animation-direction property can have the following values:
<ul>
  <li><b>normal</b> - The animation is played as normal (forwards). This is default</li>
  <li><b>reverse</b> - The animation is played in reverse direction (backwards)</li>
  <li><b>alternate</b> - The animation is played forwards first, then backwards</li>
  <li><b>alternate-reverse</b> - The animation is played backwards first, then forwards</li>
</ul>
The following example will run the animation in reverse direction (backwards):
<pre>
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-direction: reverse;
}
</pre>
The following example uses the value "alternate" to make the animation run forwards first, then backwards:
<pre>
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: 2;
  animation-direction: alternate;
}
</pre>
The following example uses the value "alternate-reverse" to make the animation run backwards first, then forwards:
<pre>
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: example;
  animation-duration: 4s;
  animation-iteration-count: 2;
  animation-direction: alternate-reverse;
}
</pre>
<h1>Speed Curve</h1>
The animation-timing-function property specifies the speed curve of the animation.
<br>
The animation-timing-function property can have the following values:
<ul>
  <li><b>ease</b> - Specifies an animation with a slow start, then fast, then end slowly (this is default)</li>
  <li><b>linear</b> - Specifies an animation with the same speed from start to end</li>
  <li><b>ease-in</b> - Specifies an animation with a slow start</li>
  <li><b>ease-out</b> - Specifies an animation with a slow end</li>
  <li><b>ease-in-out</b> - Specifies an animation with a slow start and end</li>
  <li><b>cubic-bezier(n,n,n,n)</b> - Lets you define your own values in a cubic-bezier function</li>
</ul>
The following example shows some of the different speed curves that can be used:
<pre>
#div1 {animation-timing-function: linear;}
#div2 {animation-timing-function: ease;}
#div3 {animation-timing-function: ease-in;}
#div4 {animation-timing-function: ease-out;}
#div5 {animation-timing-function: ease-in-out;}
</pre>
<h1>fill-mode</h1>
CSS animations do not affect an element before the first keyframe is played or after the last keyframe is played. The animation-fill-mode property can override this behavior.
<br>
The animation-fill-mode property specifies a style for the target element when the animation is not playing (before it starts, after it ends, or both).
<br>
The animation-fill-mode property can have the following values:
<ul>
  <li><b>none</b> - Default value. Animation will not apply any styles to the element before or after it is executing;</li>
  <li><b>forwards</b> - The element will retain the style values that is set by the last keyframe (depends on animation-direction and animation-iteration-count)</li>
  <li><b>backwards</b> - The element will get the style values that is set by the first keyframe (depends on animation-direction), and retain this during the animation-delay period</li>
  <li><b>both</b> - The animation will follow the rules for both forwards and backwards, extending the animation properties in both directions</li>
</ul>
The following example lets the <b>&lt;div&gt;</b> element retain the style values from the last keyframe when the animation ends:
<pre>
div {
  width: 100px;
  height: 100px;
  background: red;
  position: relative;
  animation-name: example;
  animation-duration: 3s;
  animation-fill-mode: forwards;
}
</pre>
The following example lets the <b>&lt;div&gt;</b> element get the style values set by the first keyframe before the animation starts (during the animation-delay period):
<pre>
div {
  width: 100px;
  height: 100px;
  background: red;
  position: relative;
  animation-name: example;
  animation-duration: 3s;
  animation-delay: 2s;
  animation-fill-mode: backwards;
}
</pre>
The following example lets the <b>&lt;div&gt;</b> element get the style values set by the first keyframe before the animation starts, and retain the style values from the last keyframe when the animation ends:
<pre>
div {
  width: 100px;
  height: 100px;
  background: red;
  position: relative;
  animation-name: example;
  animation-duration: 3s;
  animation-delay: 2s;
  animation-fill-mode: both;
}
</pre>
<h1>Shorthand</h1>
The example below uses six of the animation properties:
<pre>
div {
  animation-name: example;
  animation-duration: 5s;
  animation-timing-function: linear;
  animation-delay: 2s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}
</pre>
The same animation effect as above can be achieved by using the shorthand animation property:
<pre>
div {
  animation: example 5s linear 2s infinite alternate;
}
</pre>
