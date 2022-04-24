<a href="/JS/jQuery/Syntax.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/jQuery/Events.md">Next &gt;</a>
<hr>
jQuery was created in 2006 by John Resig. It was designed to handle Browser Incompatibilities and to simplify HTML DOM Manipulation, Event Handling, Animations, and Ajax.
<br>
For more than 10 years, jQuery has been the most popular JavaScript library in the world.
<br>
However, after JavaScript Version 5 (2009), most of the jQuery utilities can be solved with a few lines of standard JavaScript:
<h1>Finding HTML Element by Id</h1>
Return the element with <code>id="id01"</code>:
<br>
<b>jQuery:</b>
<pre>myElement = $("#id01");</pre>
<b>JavaScript:</b>
<pre>myElement = document.getElementById("id01");</pre>
<h1>Finding HTML Element by Tag</h1>
Return the <code>&lt;p&gt;</code> element:
<br>
<b>jQuery:</b>
<pre>myElement = $("p");</pre>
<b>JavaScript:</b>
<pre>myElement = document.getElementByTagName("p");</pre>
<h1>Finding HTML Element by Class</h1>
Return the element with <code>class="intro"</code>:
<br>
<b>jQuery:</b>
<pre>myElement = $(".intro");</pre>
<b>JavaScript:</b>
<pre>myElement = document.getElementByClassName("intro");</pre>
<h1>Finding HTML Element by Class</h1>
Return a list of all <code>&lt;p&gt;</code> elements with <code>class="intro"</code>:
<br>
<b>jQuery:</b>
<pre>myElement = $("p.intro");</pre>
<b>JavaScript:</b>
<pre>myElement = document.querySelectorAll("p.intro");</pre>
