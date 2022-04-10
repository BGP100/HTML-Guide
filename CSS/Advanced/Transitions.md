<a href="/CSS/Advanced/3D-Transforms.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Advanced/Animations.md">Next &gt;</a>
<hr>
CSS transitions allows you to change property values smoothly, over a given duration.
<br>
In this chapter you will learn about the following properties:
<ul>
  <li><b>transition</b></li>
  <li><b>transition-delay</b></li>
  <li><b>transition-duration</b></li>
  <li><b>transition-property</b></li>
  <li><b>transition-timing-function</b></li>
</ul>
<h1>Browser Support</h1>
The numbers in the table specify the first browser version that fully supports the property.
<table class="ws-table-all notranslate">
  <tr>
    <th>Property</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>transition</td>
    <td>26.0</td>
    <td>10.0</td>
    <td>16.0</td>
    <td>6.1</td>
    <td>12.1</td>
  </tr>
  <tr>
    <td>transition-delay</td>
    <td>26.0</td>
    <td>10.0</td>
    <td>16.0</td>
    <td>6.1</td>
    <td>12.1</td>
  </tr>
  <tr>
    <td>transition-duration</td>
    <td>26.0</td>
    <td>10.0</td>
    <td>16.0</td>
    <td>6.1</td>
    <td>12.1</td>
  </tr>
  <tr>
    <td>transition-property</td>
    <td>26.0</td>
    <td>10.0</td>
    <td>16.0</td>
    <td>6.1</td>
    <td>12.1</td>
  </tr>
  <tr>
    <td>transition-timing-function</td>
    <td>26.0</td>
    <td>10.0</td>
    <td>16.0</td>
    <td>6.1</td>
    <td>12.1</td>
  </tr>
</table>
<h1>How to Use Them?</h1>
To create a transition effect, you must specify two things:

the CSS property you want to add an effect to
the duration of the effect
Note: If the duration part is not specified, the transition will have no effect, because the default value is 0.
<br>
The following example shows a 100px * 100px red <b>&lt;div&gt;</b> element. The <b>&lt;div&gt;</b> element has also specified a transition effect for the width property, with a duration of 2 seconds:
<pre>
div {
  width: 100px;
  height: 100px;
  background: red;
  transition: width 2s;
}
</pre>
The transition effect will start when the specified CSS property (width) changes value.
<br>
Now, let us specify a new value for the width property when a user mouses over the <b>&lt;div&gt;</b> element:
<pre>
div:hover {
  width: 300px;
}
</pre>
Notice that when the cursor mouses out of the element, it will gradually change back to its original style.
<h1>Change Several Values</h1>
The following example adds a transition effect for both the width and height property, with a duration of 2 seconds for the width and 4 seconds for the height:
<pre>
div {
  transition: width 2s, height 4s;
}
</pre>
<h1>The Speed Curve of the Transition</h1>
The transition-timing-function property specifies the speed curve of the transition effect.
<br>
The transition-timing-function property can have the following values:
<ul>
  <li><b>ease</b> - specifies a transition effect with a slow start, then fast, then end slowly (this is default)</li>
  <li><b>linear</b> - specifies a transition effect with the same speed from start to end</li>
  <li><b>ease-in</b> - specifies a transition effect with a slow start</li>
  <li><b>ease-out</b> - specifies a transition effect with a slow end</li>
  <li><b>ease-in-out</b> - specifies a transition effect with a slow start and end</li>
  <li><b>cubic-bezier(n,n,n,n)</b> - lets you define your own values in a cubic-bezier function</li>
</ul>
The following example shows some of the different speed curves that can be used:
<pre>
#div1{transition-timing-function:linear;}
#div2{transition-timing-function:ease;}
#div3{transition-timing-function:ease-in;}
#div4{transition-timing-function:ease-out;}
#div5{transition-timing-function:ease-in-out;}
</pre>
<h1>Delay the Transition</h1>
The transition-delay property specifies a delay (in seconds) for the transition effect.
<br>
The following example has a 1 second delay before starting:
<pre>
div {
  transition-delay: 1s;
}
</pre>
<h1>Transition + Transformation</h1>
The following example adds a transition effect to the transformation:
<pre>
div {
  transition: width 2s, height 2s, transform 2s;
}
</pre>
<h1>More Examples</h1>
The CSS <b>transition</b> properties can be specified one by one, like this:
<pre>
div {
  transition-property: width;
  transition-duration: 2s;
  transition-timing-function: linear;
  transition-delay: 1s;
}
</pre>
The CSS <b>transition</b> properties can be specified one by one, like this:
<pre>
div {
  transition: width 2s linear 1s;
}
</pre>
