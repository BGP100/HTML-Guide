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
    <td>quote(<i>string</i>)</td>
    <td>Adds quotes to <i>string</i>, and returns the result.<br><br>
    <b>Example:</b><br>quote(Hello world!)<br>Result: "Hello world!"</td>
  </tr>
  <tr>
    <td>str-index(<i>string</i>,<i> substring</i>)</td>
    <td>Returns the index of the first occurrence of the <i>substring</i> within 
    <i>string</i>.<br><br>
    <b>Example:</b><br>str-index("Hello world!", "H")<br>Result: 1</td>
  </tr>
  <tr>
    <td>str-insert(<i>string</i>, <i>insert</i>, <i>index</i>)</td>
    <td>Returns <i>string</i> with <i>insert</i> inserted at the specified 
    <i>index</i> position.<br><br>
    <b>Example:</b><br>str-insert("Hello world!", " wonderful", 6)<br>Result: "Hello 
    wonderful world!"</td>
  </tr>
  <tr>
    <td>str-length(<i>string</i>)</td>
    <td>Returns the length of <i>string</i> (in characters).<br><br>
    <b>Example:</b><br>str-length("Hello world!")<br>Result: 12</td>
  </tr>
  <tr>
    <td>str-slice(<i>string</i>, <i>start</i>, <i>end</i>)</td>
    <td>Extracts characters from <i>string</i>; start at <i>start</i> 
    and end at <i>end</i>, and returns the slice.<br><br>
    <b>Example:</b><br>str-slice("Hello world!", 2, 
    5)<br>Result: "ello"</td>
  </tr>
  <tr>
    <td>to-lower-case(<i>string</i>)</td>
    <td>Returns a copy of <i>string</i> converted to lower case.<br><br>
    <b>Example:</b><br>to-lower-case("Hello 
    World!")<br>Result: "hello world!"</td>
  </tr>
  <tr>
    <td>to-upper-case(<i>string</i>)</td>
    <td>Returns a copy of <i>string</i> converted to upper case.<br><br>
    <strong>Example:</strong><br>to-upper-case("Hello 
    World!")<br>Result: "HELLO WORLD!"</td>
  </tr>
  <tr>
    <td>unique-id()</td>
    <td>Returns a unique randomly generated unquoted string (guaranteed to be 
    unique within the current sass session).<br><br>
    <b>Example:</b><br>unique-id()<br>Result: 
    tyghefnsv</td>
  </tr>
  <tr>
    <td>unquote(<i>string</i>)</td>
    <td>Removes quotes around <i>string</i> (if any), and returns the result.<br>
    <br>
    <b>Example:</b><br>unquote("Hello world!")<br>Result: Hello world!</td>
  </tr>
</table>
