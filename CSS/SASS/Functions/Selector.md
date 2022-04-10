<a href="/CSS/SASS/Functions/Map.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/SASS/Functions/Introspection.md">Next &gt;</a>
<hr>
The selector functions are used to check and manipulate selectors. 
<br>
The following table lists all selector functions in SASS:
<table class="ws-table-all notranslate">
  <tr>
    <th>Function</th>
    <th>Description &amp; Example</th>
  </tr>
  <tr>
    <td>is-superselector(<em>super</em>, <em>sub</em>)</td>
    <td>Checks whether the <em>super</em> selector matches all the elements that
    <em>sub</em> matches.<br><br>
    <strong>Example:</strong><br>is-superselector(&quot;div&quot;, &quot;div.myInput&quot;)<br>Result: true<br>is-superselector(&quot;div.myInput&quot;, 
    &quot;div&quot;)<br>Result: false<br>is-superselector(&quot;div&quot;, 
    &quot;div&quot;)<br>Result: true</td>
  </tr>
  <tr>
    <td>selector-append(<em>selectors</em>)</td>
    <td>Appends the second (and third/fourth etc.) selector to the first 
    selector.<br><br>
    <strong>Example:</strong><br>selector-append(&quot;div&quot;, &quot;.myInput&quot;)<br>Result: div.myInput<br>selector-append(&quot;.warning&quot;, 
    &quot;__a&quot;)<br>Result: .warning__a</td>
  </tr>
  <tr>
    <td>selector-extend(<em>selector</em>, <em>extendee</em>, <em>extender</em>)</td>
    <td>&nbsp;</td>
  </tr>
  <tr>
    <td>selector-nest(<em>selectors</em>)</td>
    <td>Returns a new selector containing a nested list of CSS selectors based 
    on the list provided.<br><br>
    <strong>Example:</strong><br>selector-nest(&quot;ul&quot;, &quot;li&quot;)<br>Result: ul li<br>selector-nest(&quot;.warning&quot;, 
    &quot;alert&quot;, &quot;div&quot;)<br>Result: .warning div, alert div</td>
  </tr>
  <tr>
    <td>selector-parse(<em>selector</em>)</td>
    <td>Returns a list of strings contained in <em>selector</em> using the same 
    format as the parent selector.<br><br>
    <strong>Example:<br></strong>selector-parse(&quot;h1 .myInput .warning&quot;)<br>Result: ('h1' '.myInput' 
    '.warning')</td>
  </tr>
  <tr>
    <td>selector-replace(<em>selector</em>, <em>original</em>, <em>replacement</em>)</td>
    <td>Returns a new selector with the selectors specified in <em>replacement</em> 
    in place of selectors specified in <em>original</em>.<br><br>
    <strong>Example:</strong><br>selector-replace(&quot;p.warning&quot;, &quot;p&quot;, &quot;div&quot;)<br>Result: div.warning</td>
  </tr>
  <tr>
    <td>selector-unify(<em>selector1</em>, <em>selector2</em>)</td>
    <td>Returns a new selector that matches only elements matched by both <em>
    selector1</em> and <em>selector2</em>.<br><br>
    <strong>Example:</strong><br>selector-unify(&quot;myInput&quot;, &quot;.disabled&quot;)<br>Result: myInput.disabled<br>
    selector-unify(&quot;p&quot;, &quot;h1&quot;)<br>Result: null</td>
  </tr>
  <tr>
    <td>simple-selectors(<em>selectors</em>)</td>
    <td>Returns a list of the individual selectors in <em>selectors</em>.<br>
    <br>
    <strong>Example:</strong><br>simple-selectors(&quot;div.myInput&quot;)<br>Result: div, .myInput<br>
    simple-selectors(&quot;div.myInput:before&quot;)<br>Result: div, .myInput, 
    :before</td>
  </tr>
</table>
