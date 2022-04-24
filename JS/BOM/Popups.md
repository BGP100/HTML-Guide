<a href="/JS/BOM/Navigator.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/BOM/Timing.md">Next &gt;</a>
<hr>
JavaScript has three kind of popup boxes: Alert box, Confirm box, and Prompt box.
<h1>Alert Box</h1>
An alert box is often used if you want to make sure information comes through to the user.
<br>
When an alert box pops up, the user will have to click "OK" to proceed.
<br>
<b>Syntax:</b>
<pre>window.alert("<i>sometext</i>");</pre>
The <b>window.alert()</b> method can be written without the window prefix.
<pre>alert("I am an alert box!");</pre>
<h1>Confirm Box</h1>
A confirm box is often used if you want the user to verify or accept something.
<br>
When a confirm box pops up, the user will have to click either "OK" or "Cancel" to proceed.
<br>
If the user clicks "OK", the box returns true. If the user clicks "Cancel", the box returns false.
<br>
<b>Syntax:</b>
<pre>window.confirm("<i>sometext</i>");</pre>
The <b>window.confirm()</b> method can be written without the window prefix.
<pre>
if (confirm("Press a button!")) {
  txt = "You pressed OK!";
} else {
  txt = "You pressed Cancel!";
}
</pre>
<h1>Prompt Box</h1>
A prompt box is often used if you want the user to input a value before entering a page.
<br>
When a prompt box pops up, the user will have to click either "OK" or "Cancel" to proceed after entering an input value.
<br>
If the user clicks "OK" the box returns the input value. If the user clicks "Cancel" the box returns null.
<br>
<b>Syntax:</b>
<pre>window.prompt("<i>sometext</i>","<i>defaultText</i>");</pre>
The window.prompt() method can be written without the window prefix.
<pre>
let person = prompt("Please enter your name", "Harry Potter");
let text;
if (person == null || person == "") {
  text = "User cancelled the prompt.";
} else {
  text = "Hello " + person + "! How are you today?";
}
</pre>
<h1>Line Breaks</h1>
To display line breaks inside a popup box, use a back-slash followed by the character n.
<pre>alert("Hello\nHow are you?");</pre>
