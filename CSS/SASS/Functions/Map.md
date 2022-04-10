<a href="/CSS/SASS/Functions/List.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/SASS/Functions/Selectors.md">Next &gt;</a>
<hr>
In SASS, the map data type represents one or more key/value pairs.
<br>
<b>Tip:</b> It is also possible to use the List functions from the previous page, with maps. Then the map will be treated as a list with two elements.
<br>
SASS maps are immutable (they cannot change). So, the map functions that return a map, will return a new map, and not change the original map.
<br>
The following table lists all map functions in SASS:
<table class="ws-table-all notranslate">
  <tr>
    <th>Function</th>
    <th>Description &amp; Example</th>
  </tr>
  <tr>
    <td>map-get(<em>map</em>, <em>key</em>)</td>
    <td>Returns the value for the specified <em>key </em>in the map.<br><br>
    <strong>Example:</strong><br>$font-sizes: (&quot;small&quot;: 12px, &quot;normal&quot;: 18px, &quot;large&quot;: 24px)<br>map-get($font-sizes, 
    &quot;small&quot;)<br>Result: 12px</td>
  </tr>
  <tr>
    <td>map-has-key(<em>map</em>, <em>key</em>)</td>
    <td>Checks whether <em>map</em> has the specified <em>key</em>. Returns true or 
    false.<br><br><strong>Example:</strong><br>$font-sizes: (&quot;small&quot;: 12px, &quot;normal&quot;: 18px, &quot;large&quot;: 24px)<br>map-has-key($font-sizes, 
    &quot;big&quot;)<br>Result: false</td>
  </tr>
  <tr>
    <td>map-keys(<em>map</em>)</td>
    <td>Returns a list of all keys in <em>map</em>.<br><br><strong>Example:</strong><br>
    $font-sizes: (&quot;small&quot;: 12px, &quot;normal&quot;: 18px, &quot;large&quot;: 24px)<br>map-keys($font-sizes)<br>Result: 
    &quot;small&quot;, &quot;normal, &quot;large&quot;</td>
  </tr>
  <tr>
    <td>map-merge(<em>map1</em>, <em>map2</em>)</td>
    <td>Appends <em>map2</em> to the end of <em>map1</em>.<br><br><strong>
    Example:</strong><br>$font-sizes: (&quot;small&quot;: 12px, &quot;normal&quot;: 18px, &quot;large&quot;: 24px)<br>
    $font-sizes2: (&quot;x-large&quot;: 30px, &quot;xx-large&quot;: 36px)<br>map-merge($font-sizes, 
    $font-sizes2)<br>Result: &quot;small&quot;: 12px, &quot;normal&quot;: 18px, &quot;large&quot;: 24px, 
    &quot;x-large&quot;: 30px, &quot;xx-large&quot;: 36px</td>
  </tr>
  <tr>
    <td>map-remove(<em>map</em>, <em>keys...</em>)</td>
    <td>Removes the specified keys from <em>map</em>.<br><br><strong>Example:</strong><br>$font-sizes: (&quot;small&quot;: 12px, &quot;normal&quot;: 18px, &quot;large&quot;: 24px)<br>map-remove($font-sizes, 
    &quot;small&quot;)<br>Result: (&quot;normal&quot;: 18px, &quot;large&quot;: 24px)<br>map-remove($font-sizes, 
    &quot;small&quot;, &quot;large&quot;)<br>Result: (&quot;normal&quot;: 18px)</td>
  </tr>
  <tr>
    <td>map-values(<em>map</em>)</td>
    <td>Returns a list of all values in <em>map</em>.<br><br><strong>Example:</strong><br>$font-sizes: (&quot;small&quot;: 12px, &quot;normal&quot;: 18px, &quot;large&quot;: 24px)<br>map-values($font-sizes)<br>Result: 
    12px, 18px, 24px</td>
  </tr>
</table>
