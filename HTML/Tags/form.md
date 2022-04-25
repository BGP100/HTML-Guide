The <b>&lt;form&gt;</b> tag is used to create an HTML form for user input.
<br>
The <b>&lt;form&gt;</b> element can contain one or more of the following form elements:
<ul>
  <li><a href="input.md">&lt;input&gt;</a></li>
  <li><a href="textarea.md">&lt;textarea&gt;</a></li>
  <li><a href="button.md">&lt;button&gt;</a></li>
  <li><a href="select.md">&lt;select&gt;</a></li>
  <li><a href="option.md">&lt;option&gt;</a></li>
  <li><a href="optgroup.md">&lt;optgroup&gt;</a></li>
  <li><a href="fieldset.md">&lt;fieldset&gt;</a></li>
  <li><a href="label.md">&lt;label&gt;</a></li>
  <li><a href="outout.md">&lt;outout&gt;</a></li>
</ul>
<pre>
&lt;form action="/action_page.php"&gt;
  &lt;fieldset&gt;
    &lt;legend&gt;Personalia:&lt;/legend&gt;
    &lt;label for="fname"&gt;First name:&lt;/label&gt;
    &lt;input type="text" id="fname" name="fname"&gt;&lt;br&gt;&lt;br&gt;
    &lt;label for="lname"&gt;Last name:&lt;/label&gt;
    &lt;input type="text" id="lname" name="lname"&gt;&lt;br&gt;&lt;br&gt;
    &lt;label for="email"&gt;Email:&lt;/label&gt;
    &lt;input type="email" id="email" name="email"&gt;&lt;br&gt;&lt;br&gt;
    &lt;label for="birthday"&gt;Birthday:&lt;/label&gt;
    &lt;input type="date" id="birthday" name="birthday"&gt;&lt;br&gt;&lt;br&gt;
    &lt;input type="submit" value="Submit"&gt;
  &lt;/fieldset&gt;
&lt;/form&gt;
</pre>
<h1>Browser Support</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>Browser</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>Compatibility</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
  </tr>
</table>
<h1>Standard</h1>
The <b>&lt;form&gt;</b> tag supports the standard attributes.
<h1>Event</h1>
The <b>&lt;form&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
Most browsers will display the <b>&lt;form&gt;</b> element with the following default values:
<pre>
form {
  display: block;
  margin-top: 0em;
}
</pre>
