Here I describe all the <b><code>form*</code></b> attributes for the <b>&lt;input&gt;</b> element.
<h1>form</h1>
The input <b>form</b> attribute specifies the form the <b>&lt;input&gt;</b> element belongs to.
<br>
The value of this attribute must be equal to the id attribute of the <b>&lt;form&gt;</b> element it belongs to.
<h1>formaction</h1>
The input <b>formaction</b> attribute specifies the URL of the file that will process the input when the form is submitted.
<br>
<b><i>Note:</i></b> This attribute overrides the <b>action</b> attribute of the <b>&lt;form&gt;</b> element.
<br>
The <b>formaction</b> attribute works with the following input types: submit and image.
<h1>formenctype</h1>
The input <b>formenctype</b> attribute specifies how the form-data should be encoded when submitted (only for forms with method="post").
<br>
<b><i>Note:</i></b> This attribute overrides the enctype attribute of the <b>&lt;form&gt;</b> element.
<br>
The <b>formenctype</b> attribute works with the following input types: submit and image.
<h1>formmethod</h1>
The input <b>formmethod</b> attribute defines the HTTP method for sending form-data to the action URL.
<br>
<b><i>Note:</i></b> This attribute overrides the method attribute of the <b>&lt;form&gt;</b> element.
<br>
The <b>formmethod</b> attribute works with the following input types: submit and image.
<br>
The form-data can be sent as URL variables (method="get") or as an HTTP post transaction (method="post").
<p></p>
<b>Notes on the "get" method:</b>
<ul>
  <li>This method appends the form-data to the URL in name/value pairs.</li>
  <li>This method is useful for form submissions where a user want to bookmark the result.</li>
  <li>There is a limit to how much data you can place in a URL (varies between browsers), therefore, you cannot be sure that all of the form-data will be correctly transferred.</li>
  <li>Never use the "get" method to pass sensitive information! (password or other sensitive information will be visible in the browser's address bar).</li>
</ul>
<b>Notes on the "post" method:</b>
<ul>
  <li>This method sends the form-data as an HTTP post transaction.</li>
  <li>Form submissions with the "post" method cannot be bookmarked.</li>
  <li>The "post" method is more robust and secure than "get", and "post" does not have size limitations.</li>
</ul>
<h1>formtarget</h1>
The input <b>formtarget</b> attribute specifies a name or a keyword that indicates where to display the response that is received after submitting the form.
<br>
<b><i>Note:</i></b> This attribute overrides the target attribute of the <b>&lt;form&gt;</b> element.
<br>
The <b>formtarget</b> attribute works with the following input types: submit and image.
<h1>formnovalidate</h1>
The input <b>formnovalidate</b> attribute specifies that an <b>&lt;input&gt;</b> element should not be validated when submitted.
<br>
<b><i>Note:</i></b> This attribute overrides the novalidate attribute of the <b>&lt;form&gt;</b> element.
<br>
The <b>formnovalidate</b> attribute works with the following input types: submit.
<h1>novalidate</h1>
The <b>novalidate</b> attribute is a <b>&lt;form&gt;</b> attribute.
<br>
When present, <b>novalidate</b> specifies that all of the form-data should not be validated when submitted.
