<ul>
  <li><a href="#action">action</a></li>
  <li><a href="#target">target</a></li>
  <li><a href="#method">method</a></li>
  <li><a href="#autocomplete">autocomplete</a></li>
  <li><a href="#novalidate">novalidate</a></li>
</ul>
<h1>action</h1>
The action attribute defines the action to be performed when the form is submitted.
<br>
Usually, the form data is sent to a file on the server when the user clicks on the submit button.
<br>
In the example below, the form data is sent to a file called "action_page.php". This file contains a server-side script that handles the form data:
<pre>
&lt;form action="/action_page.php"&gt;
  &lt;label for="fname"&gt;First name:&lt;/label&gt;
  &lt;input type="text" id="fname" name="fname" value="John"&gt;
  &lt;label for="lname"&gt;Last name:&lt;/label&gt;
  &lt;input type="text" id="lname" name="lname" value="Doe"&gt;
  &lt;p&gt;&lt;/p&gt;
  &lt;input type="submit" value="Submit"&gt;
&lt;/form&gt;
</pre>
<h1>target</h1>
The <b>target</b> attribute specifies where to display the response that is received after submitting the form.
<br>
The <b>target</b> attribute can have one of the following values:
<table class="ws-table-all notranslate"> 
  <tr>
    <th style="width:20%">Value</th>
    <th>Description</th>
  </tr>  
  <tr>
    <td>_blank</td>
    <td>The response is displayed in a new window or tab</td>
  </tr>
  <tr>
    <td>_self</td>
    <td>The response is displayed in the current window</td>
  </tr>
  <tr>
    <td>_parent</td>
    <td>The response is displayed in the parent frame</td>
  </tr>
  <tr>
    <td>_top</td>
    <td>The response is displayed in the full body of the window</td>
  </tr>
  <tr>
    <td><i>framename</i></td>
    <td>The response is displayed in a named iframe</td>
  </tr>
</table>
<h1>method</h1>
The method attribute specifies the HTTP method to be used when submitting the form data.
<br>
The form-data can be sent as URL variables (with method="get") or as HTTP post transaction (with method="post").
<br>
The default HTTP method when submitting form data is GET.
<pre>&lt;form action="/action_page.php" method="get"&gt;</pre>
<pre>&lt;form action="/action_page.php" method="post"&gt;</pre>
<b>get</b> Notes:
<ul>
  <li>Appends the form data to the URL, in name/value pairs.</li>
  <li>NEVER use GET to send sensitive data! (the submitted form data is visible in the URL!).</li>
  <li>The length of a URL is limited (2048 characters).</li>
  <li>Useful for form submissions where a user wants to bookmark the result.</li>
  <li>GET is good for non-secure data, like query strings in Google.</li>
</ul>
<b>post</b> Notes:
<ul>
  <li>Appends the form data inside the body of the HTTP request (the submitted form data is not shown in the URL).</li>
  <li>POST has no size limitations, and can be used to send large amounts of data.</li>
  <li>Form submissions with POST cannot be bookmarked.</li>
</ul>
<h1>autocomplete</h1>
The autocomplete attribute specifies whether a form should have autocomplete on or off.
<br>
When autocomplete is on, the browser automatically complete values based on values that the user has entered before.
<pre>&lt;form action="/action_page.php" autocomplete="on"&gt;</pre>
<h1>novalidate</h1>
The novalidate attribute is a boolean attribute.
<br>
When present, it specifies that the form-data (input) should not be validated when submitted.
<pre>&lt;form action="/action_page.php" novalidate&gt;</pre>
<h1>All &lt;form&gt; Attributes</h1>
<table class="ws-table-all">
 <tr>
  <th>Attribute</th>
  <th>Description</th>
 </tr>
 <tr>
  <td>accept-charset</td>
  <td>Specifies the character encodings used for form submission</td>
 </tr>
 <tr>
  <td>action</td>
  <td>Specifies where to send the form-data when a form is submitted</td>
 </tr>
 <tr>
  <td>autocomplete</td>
  <td>Specifies whether a form should have autocomplete on or off</td>
 </tr>
 <tr>
  <td>enctype</td>
  <td>Specifies how the form-data should be encoded when submitting it to the 
  server (only for method="post")</td>
 </tr>
 <tr>
  <td>method</td>
  <td>Specifies the HTTP method to use when sending form-data</td>
 </tr>
 <tr>
  <td>name</td>
  <td>Specifies the name of the form</td>
 </tr>
 <tr>
  <td>novalidate</td>
  <td>Specifies that the form should not be validated when submitted</td>
 </tr>
 <tr>
  <td>rel</td>
  <td>Specifies the relationship between a linked resource and the current 
  document</td>
 </tr>
 <tr>
  <td>target</td>
  <td>Specifies where to display the response that is received after submitting 
  the form</td>
 </tr>
</table>
