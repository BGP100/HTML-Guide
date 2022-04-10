<a href="/HTML/Forms/InputTypes.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Forms/Input-FormAttributes.md">Next &gt;</a>
<hr>
Here I describe all the attributes for the <b>&lt;input&gt;</b> element.
<h1>value</h1>
The input value attribute specifies an initial value for an input field.
<h1>readonly</h1>
The input <b>readonly</b> attribute specifies that an input field is read-only.
<br>
A read-only input field cannot be modified (however, a user can tab to it, highlight it, and copy the text from it).
<br>
The value of a read-only input field will be sent when submitting the form!
<h1>disabled</h1>
The input <b>disabled</b> attribute specifies that an input field should be disabled.
<br>
A disabled input field is unusable and un-clickable.
<br>
The value of a disabled input field will not be sent when submitting the form!
<h1>size</h1>
The input <b>size</b> attribute specifies the visible width, in characters, of an input field.
<br>
The default value for size is 20.
<br>
<b><i>Note:</i></b> The <b>size</b> attribute works with the following input types: text, search, tel, url, email, and password.
<h1>maxlength</h1>
The input <b>maxlength</b> attribute specifies the maximum number of characters allowed in an input field.
<br>
<b><i>Note:</i></b> When a <b>maxlength</b> is set, the input field will not accept more than the specified number of characters. However, this attribute does not provide any feedback. So, if you want to alert the user, you must write JavaScript code.
<h1>min</h1>
The input <b>min</b> and <b>max</b> attributes specify the minimum and maximum values for an input field.
<br>
The min and max attributes work with the following input types: number, range, date, datetime-local, month, time and week.
<br>
<b><i>Tip:</i></b> Use the <b>min</b> and <b>max</b> attributes together to create a range of legal values.
<h1>max</h1>
The input <b>min</b> and <b>max</b> attributes specify the minimum and maximum values for an input field.
<br>
The min and max attributes work with the following input types: number, range, date, datetime-local, month, time and week.
<br>
<b><i>Tip:</i></b> Use the <b>min</b> and <b>max</b> attributes together to create a range of legal values.
<h1>multiple</h1>
The input <b>multiple</b> attribute specifies that the user is allowed to enter more than one value in an input field.
<br>
The <b>multiple</b> attribute works with the following input types: email, and file.
<h1>pattern</h1>
The input <b>pattern</b> attribute specifies a regular expression that the input field's value is checked against, when the form is submitted.
<br>
The pattern attribute works with the following input types: text, date, search, url, tel, email, and password.
<br>
<b><i>Tip:</i></b> Use the <b>title</b> attribute to describe the pattern to help the user.
<h1>placeholder</h1>
The input <b>placeholder</b> attribute specifies a short hint that describes the expected value of an input field (a sample value or a short description of the expected format).
<br>
The short hint is displayed in the input field before the user enters a value.
<br>
The <b>placeholder</b> attribute works with the following input types: text, search, url, tel, email, and password.
<h1>required</h1>
The input <b>required</b> attribute specifies that an input field must be filled out before submitting the form.
<br>
The <b>required</b> attribute works with the following input types: text, search, url, tel, email, password, date pickers, number, checkbox, radio, and file.
<h1>step</h1>
The input <b>step</b> attribute specifies the legal number intervals for an input field.
<br>
<b><i>Example:</i></b> if step="3", legal numbers could be -3, 0, 3, 6, etc.
<br>
<b><i>Tip:</i></b> This attribute can be used together with the max and min attributes to create a range of legal values.
<br>
The <b>step</b> attribute works with the following input types: number, range, date, datetime-local, month, time and week.
<h1>autofocus</h1>
The input <b>autofocus</b> attribute specifies that an input field should automatically get focus when the page loads.
<h1>height</h1>
The input height and width attributes specify the height and width of an input &lt;type="image"&gt; element.
<p></p>
<b><i>Tip:</i></b> Always specify both the height and width attributes for images. If height and width are set, the space required for the image is reserved when the page is loaded. Without these attributes, the browser does not know the size of the image, and cannot reserve the appropriate space to it. The effect will be that the page layout will change during loading (while the images load).
<h1>width</h1>
The input height and width attributes specify the height and width of an input &lt;type="image"&gt; element.
<p></p>
<b><i>Tip:</i></b> Always specify both the height and width attributes for images. If height and width are set, the space required for the image is reserved when the page is loaded. Without these attributes, the browser does not know the size of the image, and cannot reserve the appropriate space to it. The effect will be that the page layout will change during loading (while the images load).
<h1>list</h1>
The input <b>list</b> attribute refers to a <a href="Elements.md#datalist">&lt;datalist&gt;</a> element that contains pre-defined options for an <b>&lt;input&gt;</b> element.
<h1>autocomplete</h1>
The input <b>autocomplete</b> attribute specifies whether a form or an input field should have autocomplete on or off.
<br>
Autocomplete allows the browser to predict the value. When a user starts to type in a field, the browser should display options to fill in the field, based on earlier typed values.
<br>
The <b>autocomplete</b> attribute works with <b>&lt;form&gt;</b> and the following <b>&lt;input&gt;</b>  types: text, search, url, tel, email, password, datepickers, range, and color.
<br>
<b><i>Tip:</i></b> In some browsers you may need to activate an autocomplete function for this to work (Look under "Preferences" in the browser's menu).
