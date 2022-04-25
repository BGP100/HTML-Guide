The <b>&lt;label&gt;</b> tag defines a label for several elements:
<ul>
  <li><code>&lt;input type="checkbox"&gt;</code></li>
  <li><code>&lt;input type="color"&gt;</code></li>
  <li><code>&lt;input type="date"&gt;</code></li>
  <li><code>&lt;input type="datetime-local"&gt;</code></li>
  <li><code>&lt;input type="email"&gt;</code></li>
  <li><code>&lt;input type="file"&gt;</code></li>
  <li><code>&lt;input type="month"&gt;</code></li>
  <li><code>&lt;input type="number"&gt;</code></li>
  <li><code>&lt;input type="password"&gt;</code></li>
  <li><code>&lt;input type="radio"&gt;</code></li>
  <li><code>&lt;input type="range"&gt;</code></li>
  <li><code>&lt;input type="search"&gt;</code></li>
  <li><code>&lt;input type="tel"&gt;</code></li>
  <li><code>&lt;input type="text"&gt;</code></li>
  <li><code>&lt;input type="time"&gt;</code></li>
  <li><code>&lt;input type="url"&gt;</code></li>
  <li><code>&lt;input type="week"&gt;</code></li>
  <li><code>&lt;meter&gt;</code></li>
  <li><code>&lt;progress&gt;</code></li>
  <li><code>&lt;select&gt;</code></li>
  <li><code>&lt;textarea&gt;</code></li>
</ul>
Proper use of labels with the elements above will benefit:
<ul>
  <li>Screen reader users (will read out loud the label, when the user is focused on the element)</li>
  <li>Users who have difficulty clicking on very small regions (such as checkboxes) - because when a user clicks the text within the <b>&lt;label&gt;</b> element, it toggles the input (this increases the hit area).</li>
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
The <b>&lt;label&gt;</b> tag supports the standard attributes.
<h1>Event</h1>
The <b>&lt;label&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
Most browsers will display the <b>&lt;label&gt;</b> element with the following default values:
<pre>
label {
  cursor: default;
}
</pre>
