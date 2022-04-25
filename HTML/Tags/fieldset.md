The <b>&lt;fieldset&gt;</b> tag is used to group related elements in a form.
<br>
The <b>&lt;fieldset&gt;</b> tag draws a box around the related elements.
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
The <b>&lt;fieldset&gt;</b> tag supports the standard attributes.
<h1>Event</h1>
The <b>&lt;fieldset&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
Most browsers will display the <b>&lt;fieldset&gt;</b> element with the following default values:
<pre>
fieldset {
  display: block;
  margin-left: 2px;
  margin-right: 2px;
  padding-top: 0.35em;
  padding-bottom: 0.625em;
  padding-left: 0.75em;
  padding-right: 0.75em;
  border: 2px groove (internal value);
}
</pre>
