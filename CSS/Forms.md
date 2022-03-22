The look of an HTML form can be greatly improved with CSS:
<br>
<img src="https://i.imgur.com/Pyt38lj.png">
<h1>Styling Inputs</h1>
Use the <b>width</b> property to determine the width of the input field:
<br>
<img src="https://i.imgur.com/kSLxCpm.png">
<pre>
input {
  width: 100%;
}
</pre>
The example above applies to all <b>&lt;input&lt;</b> elements. If you only want to style a specific input type, you can use attribute selectors:
<ul>
  <li><b>input[type=text]</b> - will only select text fields</li>
  <li><b>input[type=password]</b> - will only select password fields</li>
  <li><b>input[type=number]</b> - will only select number fields</li>
  <li><a href="https://github.com/BGP100/HTML-Guide/blob/main/HTML/Forms/InputTypes.md">Click Here</a> to see all the types.</li>
</ul>
<h1>Padding</h1>
Use the <b>padding</b> property to add space inside the text field.
<br>
<b>Tip:</b> When you have many inputs after each other, you might also want to add some margin, to add more space outside of them:
<br>
<img src="https://i.imgur.com/jSC9lih.png">
<pre>
input[type=text] {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  box-sizing: border-box;
}
</pre>
<h1>Borders</h1>
Use the <b>border</b> property to change the border size and color, and use the border-radius property to add rounded corners:
<br>
<img src="https://i.imgur.com/fYEmDd9.png">
<pre>
input[type=text] {
  border: 2px solid red;
  border-radius: 4px;
}
</pre>
If you only want a bottom border, use the <b>border-bottom</b> property:
<img src="https://i.imgur.com/Xaa5dd8.png">
<pre>
input[type=text] {
  border: none;
  border-bottom: 2px solid red;
}
</pre>
<h1>Color</h1>
Use the <b>background-color</b> property to add a background color to the input, and the color property to change the text color:
<br>
<img src="https://i.imgur.com/1FSUuWC.png">
<pre>
input[type=text] {
  background-color: #3cbc8d;
  color: white;
}
</pre>
<h1>Focus</h1>
By default, some browsers will add a blue outline around the input when it gets focus (clicked on). You can remove this behavior by adding <b>outline: none;</b> to the input.
<br>
Use the </b>:focus</b> selector to do something with the input field when it gets focus:
<br>
<img src="https://i.imgur.com/yZ2gTzY.png">
<pre>
input[type=text]:focus {
  background-color: lightblue;
}
</pre>
<img src="https://i.imgur.com/AErcaVU.png">
<pre>
input[type=text]:focus {
  border: 3px solid #555;
}
</pre>
<h1>Icon</h1>
If you want an icon inside the input, use the <b>background-image</b> property and position it with the <b>background-position</b> property. Also notice that we add a large left padding to reserve the space of the icon:
<br>
<img src="https://i.imgur.com/wQxb86r.png">
<pre>
input[type=text] {
  background-color: white;
  background-image: url('searchicon.png');
  background-position: 10px 10px;
  background-repeat: no-repeat;
  padding-left: 40px;
}
</pre>
<h1>Animated Icon</h1>
In this example we use the CSS <b>transition</b> property to animate the width of the search input when it gets focus.
<br>
You will learn more about the <b>transition</b> property later, in the <a href="CSS/Advanced/Transitions.md">Transitions chapter</a>.
<br>
<img src="https://i.imgur.com/wQxb86r.png">
<pre>
input[type=text] {
  transition: width 0.4s ease-in-out;
}
input[type=text]:focus {
  width: 100%;
}
</pre>
<h1>Texareas</h1>
<b><i>Tip:</i></b> Use the <b>resize</b> property to prevent textareas from being resized (disable the "grabber" in the bottom right corner):
<br>
<img src="https://i.imgur.com/0PsJSBm.png">
<pre>
textarea {
  width: 100%;
  height: 150px;
  padding: 12px 20px;
  box-sizing: border-box;
  border: 2px solid #ccc;
  border-radius: 4px;
  background-color: #f8f8f8;
  resize: none;
}
</pre>
<h1>Select Menus</h1>
<img src="https://i.imgur.com/AEARxch.png">
<pre>
select {
  width: 100%;
  padding: 16px 20px;
  border: none;
  border-radius: 4px;
  background-color: #f1f1f1;
}
</pre>
<h1>Buttons</h1>
<img src="https://i.imgur.com/OO5Np2L.png">
<br>
<img src="https://i.imgur.com/T4Q0SKS.png">
<pre>
input[type=button], input[type=submit], input[type=reset] {
  background-color: #04AA6D;
  border: none;
  color: white;
  padding: 16px 32px;
  text-decoration: none;
  margin: 4px 2px;
  cursor: pointer;
}
/* <b><i>Tip:</i></b> use <b>width: 100%</b> for full-width buttons */
</pre>
<h1>Responsive Form</h1>
Resize the browser window to see the effect. When the screen is less than 600px wide, make the two columns stack on top of each other instead of next to each other.
<br>
<img src="https://i.imgur.com/mcA5qqY.png">
