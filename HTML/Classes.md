<a href="/HTML/BlockAndInline.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/ID.md">Next &gt;</a>
<hr>
The HTML class attribute is used to specify a class for an HTML element.
<br>
Multiple HTML elements can share the same class.
<br>
The class attribute is often used to point to a class name in a style sheet. It can also be used by a JavaScript to access and manipulate elements with the specific class name.
<br>
In the following example we have three <b>&lt;div&gt;</b> elements with a class attribute with the value of "city". All of the three <b>&lt;div&gt;</b> elements will be styled equally according to the <b>.city</b> style definition in the head section:
<br>
<b>CSS:</b>
<pre>
.city {
  background-color: tomato;
  color: white;
  border: 2px solid black;
  margin: 20px;
  padding: 20px;
}
</pre>
<b>HTML:</b>
<pre>
&lt;div class="city"&gt;
  &lt;h2&gt;London&lt;/h2&gt;
  &lt;p&gt;London is the capital of England.&lt;/p&gt;
&lt;/div&gt;
&lt;div class="city"&gt;
  &lt;h2&gt;Paris&lt;/h2&gt;
  &lt;p&gt;Paris is the capital of France.&lt;/p&gt;
&lt;/div&gt;
&lt;div class="city"&gt;
  &lt;h2&gt;Tokyo&lt;/h2&gt;
  &lt;p&gt;Tokyo is the capital of Japan.&lt;/p&gt;
&lt;/div&gt;
</pre>
In the following example we have two <span> elements with a class attribute with the value of "note". Both <span> elements will be styled equally according to the .note style definition in the head section:
<pre>
.note {
  font-size: 120%;
  color: red;
}
</pre>
<h1>Syntax</h1>
To create a class; write a period (.) character, followed by a class name. Then, define the CSS properties within curly braces {}:
<pre>
.city {
  background-color: tomato;
  color: white;
  padding: 10px;
}
<b>Demo:</b>
&lt;element class="city"&gt;
</pre>
<h1>Multiple</h1>
HTML elements can belong to more than one class.
<br>
To define multiple classes, separate the class names with a space, e.g. &lt;div class="city main"&gt;. The element will be styled according to all the classes specified.
<br>
In the following example, the first &lt;h2&gt; element belongs to both the city class and also to the main class, and will get the CSS styles from both of the classes:
<pre>
&lt;h2 class="city main"&gt;London&lt;/h2&gt;
&lt;h2 class="city"&gt;Paris&lt;/h2&gt;
&lt;h2 class="city"&gt;Tokyo&lt;/h2&gt;
</pre>
<h1>Different Elements</h1>
Different HTML elements can point to the same class name.
<br>
In the following example, both h2 and p points to the "city" class and will share the same style:
<pre>
&lt;h2 class="city"&gt;Paris&lt;/h2&gt;
&lt;p class="city"&gt;Paris is the capital of France&lt;/p&gt;
</pre>
<h1>Classes in JavaScript</h1>
The class name can also be used by JavaScript to perform certain tasks for specific elements.
<br>
JavaScript can access elements with a specific class name with the getElementsByClassName() method:
<pre>
&lt;script&gt;
function myFunction() {
  var x = document.getElementsByClassName("city");
  for (var i = 0; i &lt; x.length; i++) {
    x[i].style.display = "none";
  }
}
&lt;/script&gt;
</pre>
