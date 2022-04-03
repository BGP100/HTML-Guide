The string functions are used to manipulate and get information about strings.
<br>
SASS strings are 1-based. The first character in a string is at index 1, not 0.
<br>
The following table lists all string functions in SASS:
<table class="ws-table-all notranslate">
  <tr>
    <th>Function</th>
    <th>Description &amp; Example</th>
  </tr>
  <tr>
    <td>quote(<em>string</em>)</td>
    <td>Adds quotes to <em>string</em>, and returns the result.<br><br>
    <strong>Example:</strong><br>quote(Hello world!)<br>Result: &quot;Hello world!&quot;</td>
  </tr>
  <tr>
    <td>str-index(<em>string</em>,<em> substring</em>)</td>
    <td>Returns the index of the first occurrence of the <em>substring</em> within 
    <em>string</em>.<br><br>
    <strong>Example:</strong><br>str-index(&quot;Hello world!&quot;, &quot;H&quot;)<br>Result: 1</td>
  </tr>
  <tr>
    <td>str-insert(<em>string</em>, <em>insert</em>, <em>index</em>)</td>
    <td>Returns <em>string</em> with <em>insert</em> inserted at the specified 
    <em>index</em> position.<br><br>
    <strong>Example:</strong><br>str-insert(&quot;Hello world!&quot;, &quot; wonderful&quot;, 6)<br>Result: &quot;Hello 
    wonderful world!&quot;</td>
  </tr>
  <tr>
    <td>str-length(<em>string</em>)</td>
    <td>Returns the length of <em>string</em> (in characters).<br><br>
    <strong>Example:</strong><br>str-length(&quot;Hello world!&quot;)<br>Result: 12</td>
  </tr>
  <tr>
    <td>str-slice(<em>string</em>, <em>start</em>, <em>end</em>)</td>
    <td>Extracts characters from <em>string</em>; start at <em>start</em> 
    and end at <em>end</em>, and returns the slice.<br><br>
    <strong>Example:</strong><br>str-slice(&quot;Hello world!&quot;, 2, 
    5)<br>Result: &quot;ello&quot;</td>
  </tr>
  <tr>
    <td>to-lower-case(<em>string</em>)</td>
    <td>Returns a copy of <em>string</em> converted to lower case.<br><br>
    <strong>Example:</strong><br>to-lower-case(&quot;Hello 
    World!&quot;)<br>Result: &quot;hello world!&quot;</td>
  </tr>
  <tr>
    <td>to-upper-case(<em>string</em>)</td>
    <td>Returns a copy of <em>string</em> converted to upper case.<br><br>
    <strong>Example:</strong><br>to-upper-case(&quot;Hello 
    World!&quot;)<br>Result: &quot;HELLO WORLD!&quot;</td>
  </tr>
  <tr>
    <td>unique-id()</td>
    <td>Returns a unique randomly generated unquoted string (guaranteed to be 
    unique within the current sass session).<br><br>
    <strong>Example:</strong><br>unique-id()<br>Result: 
    tyghefnsv</td>
  </tr>
  <tr>
    <td>unquote(<em>string</em>)</td>
    <td>Removes quotes around <em>string</em> (if any), and returns the result.<br>
    <br>
    <strong>Example:</strong><br>unquote(&quot;Hello world!&quot;)<br>Result: Hello world!</td>
  </tr>
</table>
