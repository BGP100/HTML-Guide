<a href="/CSS/SASS/Functions/Numeric.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/SASS/Functions/Map.md">Next &gt;</a>
<hr>
The list functions are used to access values in a list, combine lists, and add items to lists.
<br>
SASS lists are immutable (they cannot change). So, the list functions that return a list, will return a new list, and not change the original list.
<br>
SASS lists are 1-based. The first list item in a list is at index 1, not 0.
<br>
The following table lists all list functions in SASS:
<table class="ws-table-all notranslate">
  <tr>
    <th>Function</th>
    <th>Description &amp; Example</th>
  </tr>
  <tr>
    <td>append(<em>list</em>, <em>value</em>, [<em>separator</em>])</td>
    <td>Adds a single <em>value</em> to the end of the list. <em>separator</em> 
    can be auto, comma, or space. auto is default.<br><br>
    <strong>Example:<br></strong>append((a b c), d)<br>Result: a b c d<br>append((a b c), (d), comma)<br>
    Result: a, b, c, d</td>
  </tr>
  <tr>
    <td>index(<em>list</em>, <em>value</em>)</td>
    <td>Returns the index position for the <em>value</em> in list.<br><br>
    <strong>Example:</strong><br>index(a b c, b)<br>Result: 2<br>index(a b c, f)<br>Result: null</td>
  </tr>
  <tr>
    <td>is-bracketed(<em>list</em>)</td>
    <td>Checks whether the list has square brackets.<br><br>
    <strong>Example:</strong><br>is-bracketed([a b c])<br>Result: true <br>is-bracketed(a b c)<br>Result: 
    false</td>
  </tr>
  <tr>
    <td>join(<em>list1</em>, <em>list2</em>, [<em>separator, bracketed</em>])</td>
    <td>Appends <em>list2</em> to the end of <em>list1</em>. <em>separator</em> 
    can be auto, comma, or space. auto is default (will use the separator in the 
    first list). <em>bracketed</em> can be auto, true, or false. auto is default.<br>
    <br>
    <strong>Example:</strong><br>join(a b c, d e f)<br>Result: a b c d e f<br>join((a b c), (d e f), 
    comma)<br>Result: a, b, c, d, e, f<br>join(a b c, d e f, $bracketed: true)<br>Result: 
    [a b c d e f]</td>
  </tr>
  <tr>
    <td>length(<em>list</em>)</td>
    <td>Returns the length of the list.<br><br>
    <strong>Example:</strong><br>length(a b c)<br>Result: 3</td>
  </tr>
  <tr>
    <td>list-separator(<em>list</em>)</td>
    <td>Returns the list separator used, as a string. Can be either space or 
    comma.<br><br>
    <strong>Example:</strong><br>list-separator(a b c)<br>Result: &quot;space&quot;<br>list-separator(a, b, c)<br>
    Result: &quot;comma&quot;</td>
  </tr>
  <tr>
    <td>nth(<em>list</em>, <em>n</em>)</td>
    <td>Returns the <em>n</em>th element in the list.<br><br>
    <strong>Example:</strong><br>nth(a b c, 3)<br>Result: c</td>
  </tr>
  <tr>
    <td>set-nth(<em>list</em>, <em>n</em>, <em>value</em>)</td>
    <td>Sets the <em>n</em>th list element to the <em>value</em> specified.<br>
    <br>
    <strong>Example:</strong><br>set-nth(a b c, 2, x)<br>Result: a x c</td>
  </tr>
  <tr>
    <td>zip(<em>lists</em>)</td>
    <td>Combines lists into a single multidimensional list.<br><br>
    <strong>Example:</strong><br>zip(1px 2px 3px, solid dashed dotted, red green blue)<br>Result: 1px 
    solid red, 2px dashed green, 3px dotted blue</td>
  </tr>
</table>
