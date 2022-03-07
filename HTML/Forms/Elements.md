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
<h1>button</h1>
<h1>fieldset</h1>
<h1>legend</h1>
<h1>datalist</h1>
<h1>output</h1>
<h1>optgroup</h1>
