The HTML <b>&lt;form&gt;</b> element can contain one or more of the following form elements:
<ul>
  <li><a href="#input">&lt;input&gt;</a></li>
  <li><a href="#label">&lt;label&gt;</a></li>
  <li><a href="#select">&lt;select&gt;</a></li>
  <li><a href="#option">&lt;option&gt;</a></li>
  <li><a href="#textarea">&lt;textarea&gt;</a></li>
  <li><a href="#button">&lt;button&gt;</a></li>
  <li><a href="#fieldset">&lt;fieldset&gt;</a></li>
  <li><a href="#legend">&lt;legend&gt;</a></li>
  <li><a href="#datalist">&lt;datalist&gt;</a></li>
  <li><a href="#output">&lt;output&gt;</a></li>
  <li><a href="#optgroup">&lt;optgroup&gt;</a></li>
</ul>
<h1>input</h1>
One of the most used form element is the <b>&lt;input&gt;</b> element.
<br>
The <b>&lt;input&gt;</b> element can be displayed in several ways, depending on the type attribute.
<pre>
&lt;label for="fname"&gt;First name:&lt;/label&gt;
&lt;input type="text" id="fname" name="fname"&gt;
</pre>
<a href="InputTypes.md">Input Types</a> Chapter.
<h1>label</h1>
The <b>&lt;label&gt;</b> element defines a label for several form elements.
<br>
The <b>&lt;label&gt;</b> element is useful for screen-reader users, because the screen-reader will read out loud the label when the user focus on the input element.
<br>
The <b>&lt;label&gt;</b> element also help users who have difficulty clicking on very small regions (such as radio buttons or checkboxes) - because when the user clicks the text within the <b>&lt;label&gt;</b> element, it toggles the radio button/checkbox.
<br>
The <b>for</b> attribute of the <b>&lt;label&gt;</b> tag should be equal to the <b>id</b> attribute of the <b>&lt;label&gt;</b> element to bind them together.
<h1>select</h1>
The <b>&lt;select&gt;</b> element defines a drop-down list:
<pre>
&lt;label for="cars"&gt;Choose a car:&lt;/label&gt;
&lt;select id="cars" name="cars"&gt;
  &lt;option value="volvo"&gt;Volvo&lt;/option&gt;
  &lt;option value="saab"&gt;Saab&lt;/option&gt;
  &lt;option value="fiat"&gt;Fiat&lt;/option&gt;
  &lt;option value="audi"&gt;Audi&lt;/option&gt;
&lt;/select&gt;
</pre>
<h1>option</h1>
The <b>&lt;select&gt;</b> elements defines an option that can be selected.
<br>
By default, the first item in the drop-down list is selected.
<br>
To define a pre-selected option, add the selected attribute to the option:
<pre>&lt;option value="fiat" selected&gt;Fiat&lt;/option&gt;</pre>
<h2>Visible Values</h2>
Use the <b>size</b> attribute to specify the number of visible values:
<pre>
&lt;label for="cars"&gt;Choose a car:&lt;/label&gt;
&lt;select id="cars" name="cars" <b>size="3"</b>&gt;
  &lt;option value="volvo"&gt;Volvo&lt;/option&gt;
  &lt;option value="saab"&gt;Saab&lt;/option&gt;
  &lt;option value="fiat"&gt;Fiat&lt;/option&gt;
  &lt;option value="audi"&gt;Audi&lt;/option&gt;
&lt;/select&gt;
</pre>
<h2>Multiple Selections</h2>
Use the <b>multiple</b> attribute to allow the user to select more than one value:
<pre>
&lt;label for="cars"&gt;Choose a car:&lt;/label&gt;
&lt;select id="cars" name="cars" size="3" <b>multiple</b>&gt;
  &lt;option value="volvo"&gt;Volvo&lt;/option&gt;
  &lt;option value="saab"&gt;Saab&lt;/option&gt;
  &lt;option value="fiat"&gt;Fiat&lt;/option&gt;
  &lt;option value="audi"&gt;Audi&lt;/option&gt;
&lt;/select&gt;
</pre>
<h1>textarea</h1>
The <b>&lt;textarea&gt;</b> element defines a multi-line input field (a text area):
<pre>&lt;textarea name="message" rows="10" cols="30"&gt;The cat was playing in the garden.&lt;/textarea&gt;</pre>
The <b>rows</b> attribute specifies the visible number of lines in a text area.
<br>
The <b>cols</b> attribute specifies the visible width of a text area.
<br>
This is how the HTML code above will be displayed in a browser:
<br>
<img src="https://i.imgur.com/PGEeeS7.jpg" width="20%">
<br>
You can also define the size of the text area by using CSS:
<pre>&lt;textarea name="message" style="width:200px;height:600px;"&gt;The cat was playing in the garden.&lt;/textarea&gt;</pre>
<h1>button</h1>
<pre>&lt;a href="image.jpg"&gt;&lt;button type="button"&gt;Click Me!&lt;/button&gt;&lt;/a&gt;</pre>
This is how the HTML code above will be displayed in a browser:
<br>
<img src="https://i.imgur.com/UDAKBtD.jpg" width="10%">
<h1>fieldset</h1>
The <b>&lt;fieldset&gt;</b> element is used to group related data in a form.
<br>
The <b>&lt;legend&gt;</b> element defines a caption for the <b>&lt;fieldset&gt;</b> element.
<pre>
&lt;form action="/action_page.php"&gt;
  <b>&lt;fieldset&gt;</b>
    &lt;legend&gt;Personalia:&lt;/legend&gt;
    &lt;label for="fname">First name:&lt;/label
    &lt;br&gt;
    &lt;input type="text" id="fname" name="fname" value="John"&gt;
    &lt;br&gt;
    &lt;label for="lname"&gt;Last name:&lt;/label&gt;
    &lt;br&gt;
    &lt;input type="text" id="lname" name="lname" value="Doe"&gt;
    &lt;br&gt;
    &lt;br&gt;
    &lt;input type="submit" value="Submit"&gt;
  <b>&lt;/fieldset&gt;</b>
&lt;/form&gt;
</pre>
This is how the HTML code above will be displayed in a browser:
<br>
<img src="https://i.imgur.com/DWcPupy.jpg" width="69%">
<h1>legend</h1>
The <b>&lt;fieldset&gt;</b> element is used to group related data in a form.
<br>
The <b>&lt;legend&gt;</b> element defines a caption for the <b>&lt;fieldset&gt;</b> element.
<pre>
&lt;form action="/action_page.php"&gt;
  <b>&lt;fieldset&gt;</b>
    &lt;legend&gt;Personalia:&lt;/legend&gt;
    &lt;label for="fname">First name:&lt;/label
    &lt;br&gt;
    &lt;input type="text" id="fname" name="fname" value="John"&gt;
    &lt;br&gt;
    &lt;label for="lname"&gt;Last name:&lt;/label&gt;
    &lt;br&gt;
    &lt;input type="text" id="lname" name="lname" value="Doe"&gt;
    &lt;br&gt;
    &lt;br&gt;
    &lt;input type="submit" value="Submit"&gt;
  <b>&lt;/fieldset&gt;</b>
&lt;/form&gt;
</pre>
This is how the HTML code above will be displayed in a browser:
<br>
<img src="https://i.imgur.com/DWcPupy.jpg" width="69%">
<h1>datalist</h1>
The <b>&lt;datalist&gt;</b> element specifies a list of pre-defined options for an <b>&lt;input&gt;</b> element.
<br>
Users will see a drop-down list of the pre-defined options as they input data.
<br>
The list attribute of the <b>&lt;input&gt;</b> element, must refer to the id attribute of the <b>&lt;datalist&gt;</b> element.
<pre>
&lt;form action="/action_page.php"&gt;
  &lt;input list="browsers"&gt;
  &lt;datalist id="browsers"&gt;
    &lt;option value="Internet Explorer"&gt;
    &lt;option value="Firefox"&gt;
    &lt;option value="Chrome"&gt;
    &lt;option value="Opera"&gt;
    &lt;option value="Safari"&gt;
  &lt;/datalist&gt;
&lt;/form&gt;
</pre>
<h1>output</h1>
The <b>&lt;output&gt;</b> element represents the result of a calculation (like one performed by a script).
<pre>
&lt;form action="/action_page.php" oninput="x.value=parseInt(a.value)+parseInt(b.value)"&gt;
  0
  &lt;input type="range"  id="a" name="a" value="50"&gt;
  100 +
  &lt;input type="number" id="b" name="b" value="50"&gt;
  =
  &lt;output name="x" for="a b"&gt;&lt;/output&gt;
  &lt;br&gt;
  &lt;br&gt;
  &lt;input type="submit"&gt;
&lt;/form&gt;
</pre>
<h1>optgroup</h1>
The <b>&lt;optgroup&gt;</b> tag is used to group related options in a <b>&lt;select&gt;</b> element (drop-down list).
<br>
If you have a long list of options, groups of related options are easier to handle for a user.
