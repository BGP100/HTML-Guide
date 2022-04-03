The introspection functions are rarely used when building a stylesheet. However, they are valuable if something does not work properly - to figure out what's going on: like debugging functions.
<br>
The following table lists all introspection functions in SASS:
<table class="ws-table-all notranslate">
  <tr>
    <th>Function</th>
    <th>Description &amp; Example</th>
  </tr>
  <tr>
    <td>call(<em>function</em>, <em>arguments</em>...)</td>
    <td>Calls a function with arguments, and returns the result.</td>
  </tr>
  <tr>
    <td>content-exists()</td>
    <td>Checks whether the current mixin was passed a @content block.</td>
  </tr>
  <tr>
    <td>feature-exists(<em>feature</em>)</td>
    <td>Checks whether <em>feature</em> is supported by the current Sass 
    implementation.<br><br>
    <strong>Example:</strong><br>feature-exists(&quot;at-error&quot;);<br>Result: true</td>
  </tr>
  <tr>
    <td>function-exists(<em>functionname</em>)</td>
    <td>Checks whether the specified function exists.<br><br>
    <strong>Example:</strong><br>function-exists(&quot;nonsense&quot;)<br>Result: false</td>
  </tr>
  <tr>
    <td>get-function(<em>functionname</em>, css: false)</td>
    <td>Returns the specified function. If css is true, it returns a plain CSS 
    function instead.</td>
  </tr>
  <tr>
    <td>global-variable-exists(<em>variablename</em>)</td>
    <td>Checks whether the specified global variable exists.<br><br>
    <strong>Example:</strong><br>variable-exists(a)<br>Result: true</td>
  </tr>
  <tr>
    <td>inspect(<em>value</em>)</td>
    <td>Returns a string representation of <em>value</em>.</td>
  </tr>
  <tr>
    <td>mixin-exists(<em>mixinname</em>)</td>
    <td>Checks whether the specified mixin exists.<br><br>
    <strong>Example:</strong><br>mixin-exists(&quot;important-text&quot;)<br>Result: true</td>
  </tr>
  <tr>
    <td>type-of(<em>value</em>)</td>
    <td>Returns the type of <em>value</em>. Can be number, string, color, list, 
    map, bool, null, function, arglist.<br><br>
    <strong>Example:</strong><br>type-of(15px)<br>Result: number<br>type-of(#ff0000)<br>Result: color</td>
  </tr>
  <tr>
    <td>unit(<em>number</em>)</td>
    <td>Returns the unit associated with a number.<br><br>
    <strong>Example:</strong><br>unit(15px)<br>Result: px</td>
  </tr>
  <tr>
    <td>unitless(<em>number</em>)</td>
    <td>Checks whether the specified number has a unit associated with it.<br>
    <br>
    <strong>Example:</strong><br>unitless(15px)<br>Result: false<br>unitless(15)<br>Result: true</td>
  </tr>
  <tr>
    <td>variable-exists(<em>variablename</em>)</td>
    <td>Checks whether the specified variable exists in the current scope.<br>
    <br>
    <strong>Example:</strong><br>variable-exists(b)<br>Result: true</td>
  </tr>
</table>
