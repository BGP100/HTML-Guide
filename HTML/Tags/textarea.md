The <b>&lt;textarea&gt;</b> tag defines a multi-line text input control.
<br>
The <b>&lt;textarea&gt;</b> element is often used in a form, to collect user inputs like comments or reviews.
<br>
A text area can hold an unlimited number of characters, and the text renders in a fixed-width font (usually Courier).
<br>
The size of a text area is specified by the <b>cols</b> and <b>rows</b> attributes (or with CSS).
<br>
The <b>name</b> attribute is needed to reference the form data after the form is submitted (if you omit the name attribute, no data from the text area will be submitted).
<br>
The <b>id</b> attribute is needed to associate the text area with a label. 
<br>
<b>Tip:</b> Always add the <a href="label.md">&lt;label&gt;</a> tag for best accessibility practices!
<pre>
&lt;label for="w3review"&gt;Review of BledyGuides:&lt;/label&gt;
&lt;textarea id="w3review" name="w3review" rows="4" cols="50"&gt;
At bledyguides.repl.co you will learn anything about programming. They offer free tutorials in (almost) all web development technologies.
&lt;/textarea&gt;
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
The <b>&lt;textarea&gt;</b> tag supports the standard attributes.
<h1>Event</h1>
The <b>&lt;textarea&gt;</b> tag supports the event attributes.
<h1>Default CSS</h1>
None.
