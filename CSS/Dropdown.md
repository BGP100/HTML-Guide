Create a hoverable dropdown with CSS.
<h1>Basic</h1>
Create a dropdown box that appears when the user moves the mouse over an element.
<pre>
&lt;style&gt;
.dropdown {
  position: relative;
  display: inline-block;
}
.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f9f9f9;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  padding: 12px 16px;
  z-index: 1;
}
.dropdown:hover .dropdown-content {
  display: block;
}
&lt;/style&gt;
&lt;div class="dropdown"&gt;
  &lt;span&gt;Mouse over me&lt;/span&gt;
  &lt;div class="dropdown-content"&gt;
    &lt;p&gt;Hello World!&lt;/p&gt;
  &lt;/div&gt;
&lt;/div&gt;
</pre>
<b>Explained:</b>
<br>
<b>(HTML)</b> Use any element to open the dropdown content, e.g. a <b>&lt;span&gt;</b>, or a <b>&lt;button&gt;</b> element.
<br>
Use a container element (like <b>&lt;div&gt;</b>) to create the dropdown content and add whatever you want inside of it.
<br>
Wrap a <b>&lt;div&gt;</b> element around the elements to position the dropdown content correctly with CSS.
<br>
<b>(CSS)</b> The <b>.dropdown</b> class uses <b>position:relative</b>, which is needed when we want the dropdown content to be placed right below the dropdown button (using <b>position:absolute</b>).
<br>
The <b>.dropdown-content</b> class holds the actual dropdown content. It is hidden by default, and will be displayed on hover (see below). Note the min-width is set to 160px. Feel free to change this.
<br>
<b>Tip:</b> If you want the width of the dropdown content to be as wide as the dropdown button, set the <b>width</b> to 100% (and <b>overflow:auto</b> to enable scroll on small screens).
<br>
Instead of using a border, we have used the CSS box-shadow property to make the dropdown menu look like a "card".
<br>
The <b>:hover</b> selector is used to show the dropdown menu when the user moves the mouse over the dropdown button.
<h1>Menu</h1>
This example is similar to the previous one, except that we add links inside the dropdown box and style them to fit a styled dropdown button:
<pre>
&lt;style&gt;
/* Style The Dropdown Button */
.dropbtn {
  background-color: #4CAF50;
  color: white;
  padding: 16px;
  font-size: 16px;
  border: none;
  cursor: pointer;
}
/* The container &lt;div&gt; - needed to position the dropdown content */
.dropdown {
  position: relative;
  display: inline-block;
}
/* Dropdown Content (Hidden by Default) */
.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f9f9f9;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
}
/* Links inside the dropdown */
.dropdown-content a {
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
}
/* Change color of dropdown links on hover */
.dropdown-content a:hover {background-color: #f1f1f1}
/* Show the dropdown menu on hover */
.dropdown:hover .dropdown-content {
  display: block;
}
/* Change the background color of the dropdown button when the dropdown content is shown */
.dropdown:hover .dropbtn {
  background-color: #3e8e41;
}
&lt;/style&gt;
&lt;div class="dropdown"&gt;
  &lt;button class="dropbtn"&gt;Dropdown&lt;/button&gt;
  &lt;div class="dropdown-content"&gt;
    &lt;a href="#"&gt;Link 1&lt;/a&gt;
    &lt;a href="#"&gt;Link 2&lt;/a&gt;
    &lt;a href="#"&gt;Link 3&lt;/a&gt;
  &lt;/div&gt;
&lt;/div&gt;
</pre>
<h1>Align</h1>
If you want the dropdown menu to go from right to left, add <b>right: 0;</b> or <b>left: 0;</b>.
<pre>
.dropdown-content-l {
  left: 0;
}
.dropdown-content-r {
  right: 0;
}
</pre>
<h1>Example</h1>
<img src="https://i.imgur.com/JVutkwr.png">
