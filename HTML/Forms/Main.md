An HTML form is used to collect user input. The user input is most often sent to a server for processing.
<br>
<img src="https://i.imgur.com/UQpQJET.png">
<h1>form Element</h1>
The HTML <b>&lt;form&gt;</b> element is used to create an HTML form for user input:
<pre>
&lt;form&gt;
.
<i>form elements</i>
.
&lt;/form&gt;
</pre>
The <b>&lt;form&gt;</b> element is a container for different types of input elements, such as: text fields, checkboxes, radio buttons, submit buttons, etc.
<h1>input Element</h1>
Here are some types:
<table class="ws-table-all">
  <tr>
    <th>Type</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>&lt;input type="text"&gt;</td>
    <td>Displays a single-line text input field</td>
  </tr>
  <tr>
    <td>&lt;input type="radio"&gt;</td>
    <td>Displays a radio button (for selecting one of many choices)</td>
  </tr>
  <tr>
    <td>&lt;input type="checkbox"&gt;</td>
    <td>Displays a checkbox (for selecting zero or more of many choices)</td>
  </tr>
  <tr>
    <td>&lt;input type="submit"&gt;</td>
    <td>Displays a submit button (for submitting the form)</td>
  </tr>
  <tr>
    <td>&lt;input type="button"&gt;</td>
    <td>Displays a clickable button</td>
  </tr>
</table>
Every type is on the <a href="InputTypes.md">Input Types</a>
<h1>name Atributte</h1>
Notice that each input field must have a <b>name</b> attribute to be submitted.
<br>
If the <b>name</b> attribute is omitted, the value of the input field will not be sent at all.
<pre>
&lt;form action="/action_page.php"&gt;
  &lt;label for="fname"&gt;First name:&lt;/label&gt;
  &lt;br&gt;
  &lt;input type="text" id="fname" value="John"&gt;
  &lt;p&gt;&lt;/p&gt;
  &lt;input type="submit" value="Submit"&gt;
&lt;/form&gt;
</pre>
