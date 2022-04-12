<a href="/JS/RegExp.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Scope.md">Next &gt;</a>
<hr>
The <b>try</b> statement defines a code block to run (to try).
<br>
The <b>catch</b> statement defines a code block to handle any error.
<br>
The <b>finally</b> statement defines a code block to run regardless of the result.
<br>
The <b>throw</b> statement defines a custom error.
<h1>URI Error</h1>
A URIError (Uniform Resource Identifier Error) is thrown if you use illegal characters in a URI function:
<pre>
try {
  decodeURI("%%%");   // You cannot URI decode percent signs
}
catch(err) {
  document.getElementById("demo").innerHTML = err.name;
}
</pre>
<h1>Non-Standard Error Object Properties</h1>
Mozilla and Microsoft defines some non-standard error object properties:
<ul>
  <li>fileName (Mozilla)</li>
  <li>lineNumber (Mozilla)</li>
  <li>columnNumber (Mozilla)</li>
  <li>stack (Mozilla)</li>
  <li>description (Microsoft)</li>
  <li>number (Microsoft)</li>
</ul>
Do not use these properties in public web sites. They will not work in all browsers.
