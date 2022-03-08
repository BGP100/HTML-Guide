In HTML, any element can be dragged and dropped.
<br>
<img src="https://i.imgur.com/N5Flb2v_d.png" draggable="true">
<br>
Drag my profile image.
<hr>
Drag and drop is a very common feature. It is when you "grab" an object and put it to a different location.
<h1>Browser Support</h1>
The numbers in the table specify the first browser version that fully supports Drag and Drop.
<table class="ws-table-all notranslate">
  <tr>
    <th>Browser</th>
    <td>Chrome</td>
    <td>Edge</td>
    <td>Firefox</td>
    <td>Safari</td>
    <td>Opera</td>
  </tr>
  <tr>
    <th>Version</th>
    <td>4.0</td>
    <td>9.0</td>
    <td>3.5</td>
    <td>6.0</td>
    <td>12.0</td>
  </tr>
</table>
<h1>Example</h1>
The example below is a simple drag and drop example:
<br>
<b>JS:</b>
<pre>
&lt;script&gt;
function allowDrop(ev) {
  ev.preventDefault();
}
function drag(ev) {
  ev.dataTransfer.setData("text", ev.target.id);
}
function drop(ev) {
  ev.preventDefault();
  var data = ev.dataTransfer.getData("text");
  ev.target.appendChild(document.getElementById(data));
}
&lt;/script&gt;
</pre>
<b>HTML:</b>
<pre>
&lt;div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)"&gt;&lt;/div&lt;
&lt;img id="drag1" src="img_logo.gif" draggable="true" ondragstart="drag(event)" width="336" height="69"&gt;
</pre>
It might seem complicated, but lets go through all the different parts of a drag and drop event.
<h1>All the Different Parts of a Drag and Drop Event</h1>
<h2>Make an Element</h2>
First of all: To make an element draggable, set the draggable attribute to true:
<pre>&lt;img draggable="true"&gt;</pre>
<h2>What to Drag?</h2>
Then, specify what should happen when the element is dragged.
<br>
In the example above, the <b>ondragstart</b> attribute calls a function, drag(event), that specifies what data to be dragged.
<br>
The <b>dataTransfer.setData()</b> method sets the data type and the value of the dragged data:
<pre>
function drag(ev) {
  ev.dataTransfer.setData("text", ev.target.id);
}
</pre>
In this case, the data type is "text" and the value is the id of the draggable element ("drag1").
<h2>Where to Drop?</h2>
The <b>ondragover</b> event specifies where the dragged data can be dropped.
<br>
By default, data/elements cannot be dropped in other elements. To allow a drop, we must prevent the default handling of the element.
<br>
This is done by calling the <b>event.preventDefault()</b> method for the ondragover event:
<pre>event.preventDefault()</pre>
<h2>Do the Drop</h2>
When the dragged data is dropped, a drop event occurs.
<br>
In the example above, the ondrop attribute calls a function, drop(event):
<pre>
function drop(ev) {
  ev.preventDefault();
  var data = ev.dataTransfer.getData("text");
  ev.target.appendChild(document.getElementById(data));
}
</pre>
Code Explained:
<ul>
  <li>Call preventDefault() to prevent the browser default handling of the data (default is open as link on drop).</li>
  <li>Get the dragged data with the dataTransfer.getData() method. This method will return any data that was set to the same type in the setData() method.</li>
  <li>The dragged data is the id of the dragged element ("drag1").</li>
  <li>Append the dragged element into the drop element.</li>
</ul>
<h2>Result</h2>
Drag my profile image.
<br>
<img src="https://i.imgur.com/N5Flb2v_d.png" draggable="true">
