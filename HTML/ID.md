<a href="/HTML/Classes.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Iframe.md">Next &gt;</a>
<hr>
The HTML id attribute is used to specify a unique id for an HTML element.
<br>
You cannot have more than one element with the same id in an HTML document.
<br>
The id attribute specifies a unique id for an HTML element. The value of the id attribute must be unique within the HTML document.
<br>
The id attribute is used to point to a specific style declaration in a style sheet. It is also used by JavaScript to access and manipulate the element with the specific id.
<br>
The syntax for id is: write a hash character (#), followed by an id name. Then, define the CSS properties within curly braces {}.
<br>
In the following example we have an h1 element that points to the id name "myHeader". This h1 element will be styled according to the #myHeader style definition in the head section:
<pre>
&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;style&gt;
      #myHeader {
        background-color: lightblue;
        color: black;
        padding: 40px;
        text-align: center;
      }
    &lt;/style&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1 id="myHeader"&gt;My Header&lt;/h1&gt;
  &lt;/body&gt;
&lt;/html&gt;
</pre>
<h1>Difference Between Class and ID</h1>
A class name can be used by multiple HTML elements, while an id name must only be used by one HTML element within the page:
<pre>
&lt;style&gt;
/* Style the element with the id "myHeader" */
#myHeader {
  background-color: lightblue;
  color: black;
  padding: 40px;
  text-align: center;
}

/* Style all elements with the class name "city" */
.city {
  background-color: tomato;
  color: white;
  padding: 10px;
}
&lt;/style&gt;

&lt;!-- An element with a unique id --&gt;
&lt;h1 id="myHeader">My Cities&lt;/h1&gt;

&lt;!-- Multiple elements with same class --&gt;
&lt;h2 class="city"&gt;London&lt;/h2&gt;
&lt;p&gt;London is the capital of England.&lt;/p&gt;

&lt;h2 class="city"&gt;Paris&lt;/h2&gt;
&lt;p&gt;Paris is the capital of France.&lt;/p&gt;

&lt;h2 class="city"&gt;Tokyo&lt;/h2&gt;
&lt;p&gt;Tokyo is the capital of Japan.&lt;/p&gt;
</pre>
<h1>Bookmarks</h1>
HTML bookmarks are used to allow readers to jump to specific parts of a webpage.
<br>
Bookmarks can be useful if your page is very long.
<br>
To use a bookmark, you must first create it, and then add a link to it.
<br>
Then, when the link is clicked, the page will scroll to the location with the bookmark.
<br>
<b>Examples:</b>
<br>
First, create a bookmark with the id attribute:
<pre>&lt;h2 id="C4"&gt;Chapter 4&lt;/h2&gt;</pre>
Then, add a link to the bookmark ("Jump to Chapter 4"), from within the same page:
<pre>&lt;a href="#C4"&gt;Jump to Chapter 4&lt;/a&gt;</pre>
<h1>ID's in JavaScript</h1>
The id attribute can also be used by JavaScript to perform some tasks for that specific element.
<br>
JavaScript can access an element with a specific id with the getElementById() method:
<pre>
&lt;script&gt;
function displayResult() {
  document.getElementById("myHeader").innerHTML = "Have a nice day!";
}
&lt;/script&gt;
</pre>
