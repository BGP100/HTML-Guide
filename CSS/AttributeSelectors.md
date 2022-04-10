<a href="/CSS/ImageSprites.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Forms.md">Next &gt;</a>
<hr>
It is possible to style HTML elements that have specific attributes or attribute values.
<h1>[attribute]</h1>
The <b>[attribute]</b> selector is used to select elements with a specified attribute.
<br>
The following example selects all <b>&lt;a&gt;</b> elements with a target attribute:
<pre>
a[target] {
  background-color: yellow;
}
</pre>
<h1>[attribute="value"]</h1>
The <b>[attribute="value"]</b> selector is used to select elements with a specified attribute and value.
<br>
The following example selects all <b>&lt;a&gt;</b> elements with a <b>target="_blank"</b> attribute:
<pre>
a[target="_blank"] {
  background-color: yellow;
}
</pre>
<h1>[attribute~="value"]</h1>
The <b>[attribute~="value"]</b> selector is used to select elements with an attribute value containing a specified word.
<br>
The following example selects all elements with a title attribute that contains a space-separated list of words, one of which is "flower":
<pre>
[title~="flower"] {
  border: 5px solid yellow;
}
</pre>
The example above will match elements with title="flower", title="summer flower", and title="flower new", but not title="my-flower" or title="flowers".
<h1>[attribute|="value"]</h1>
The <b>[attribute|="value"]</b> selector is used to select elements with the specified attribute, whose value can be exactly the specified value, or the specified value followed by a hyphen (-).
<br>
<b>Note:</b> The value has to be a whole word, either alone, like class="top", or followed by a hyphen( - ), like class="top-text".
<pre>
[class|="top"] {
  background: yellow;
}
</pre>
<h1>[attribute^="value"]</h1>
The <b>[attribute^="value"]</b> selector is used to select elements with the specified attribute, whose value starts with the specified value.
<br>
The following example selects all elements with a class attribute value that starts with "top":
<br>
<b>Note:</b> The value does not have to be a whole word!
<pre>
[class^="top"] {
  background: yellow;
}
</pre>
<h1>[attribute$="value"]</h1>
The <b>[attribute$="value"]</b> selector is used to select elements whose attribute value ends with a specified value.
<br>
The following example selects all elements with a class attribute value that ends with "test":
<br>
<b>Note:</b> The value does not have to be a whole word!
<pre>
[class$="test"] {
  background: yellow;
}
</pre>
<h1>[attribute*="value"]</h1>
The <b>[attribute*="value"]</b> selector is used to select elements whose attribute value contains a specified value.
<br>
The following example selects all elements with a class attribute value that contains "te":
<br>
<b>Note:</b> The value does not have to be a whole word!
<pre>
[class*="te"] {
  background: yellow;
}
</pre>
<h1>Style Forms</h1>
The attribute selectors can be useful for styling forms without class or ID:
<pre>
input[type="text"] {
  width: 150px;
  display: block;
  margin-bottom: 10px;
  background-color: yellow;
}
input[type="button"] {
  width: 120px;
  margin-left: 35px;
  display: block;
}
</pre>
