HTML tables allow web developers to arrange data into rows and columns.
<table class="ws-table-all notranslate">
  <tr>
    <th>Company</th>
    <th>Contact</th>
    <th>Country</th>
  </tr>
  <tr>
    <td>Alfreds Futterkiste</td>
    <td>Maria Anders</td>
    <td>Germany</td>
  </tr>
  <tr>
    <td>Centro comercial Moctezuma</td>
    <td>Francisco Chang</td>
    <td>Mexico</td>
  </tr>
  <tr>
    <td>Ernst Handel</td>
    <td>Roland Mendel</td>
    <td>Austria</td>
  </tr>
  <tr>
    <td>Island Trading</td>
    <td>Helen Bennett</td>
    <td>UK</td>
  </tr>
  <tr>
    <td>Laughing Bacchus Winecellars</td>
    <td>Yoshi Tannamuri</td>
    <td>Canada</td>
  </tr>
  <tr>
    <td>Magazzini Alimentari Riuniti</td>
    <td>Giovanni Rovelli</td>
    <td>Italy</td>
  </tr>
</table>
<h1>Define HTML Tables</h1>
A table in HTML consists of table cells inside rows and columns.
<pre>
&lt;table class="ws-table-all notranslate"&gt;
  &lt;tr&gt;
    &lt;th&gt;Company&lt;/th&gt;
    &lt;th&gt;Contact&lt;/th&gt;
    &lt;th&gt;Country&lt;/th&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;Alfreds Futterkiste&lt;/td&gt;
    &lt;td&gt;Maria Anders&lt;/td&gt;
    &lt;td&gt;Germany&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;Centro comercial Moctezuma&lt;/td&gt;
    &lt;td&gt;Francisco Chang&lt;/td&gt;
    &lt;td&gt;Mexico&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;Ernst Handel&lt;/td&gt;
    &lt;td&gt;Roland Mendel&lt;/td&gt;
    &lt;td&gt;Austria&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;Island Trading&lt;/td&gt;
    &lt;td&gt;Helen Bennett&lt;/td&gt;
    &lt;td&gt;UK&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;Laughing Bacchus Winecellars&lt;/td&gt;
    &lt;td&gt;Yoshi Tannamuri&lt;/td&gt;
    &lt;td&gt;Canada&lt;/td&gt;
  &lt;/tr&gt;
  &lt;tr&gt;
    &lt;td&gt;Magazzini Alimentari Riuniti&lt;/td&gt;
    &lt;td&gt;Giovanni Rovelli&lt;/td&gt;
    &lt;td&gt;Italy&lt;/td&gt;
  &lt;/tr&gt;
&lt;/table&gt;
</pre>
<h1>Rows</h1>
Each table row is defined by a <b>&lt;tr&gt;</b> and a <b>&lt;/tr&gt;</b> tag.
<h1>Cells</h1>
Each table cell is defined by a <b>&lt;td&gt;</b> and a <b>&lt;/td&gt;</b> tag.
<h1>Headers</h1>
Sometimes you want your cells to be headers, in those cases use the <b>&lt;th&gt;</b> tag instead of the <b>&lt;td&gt;</b> tag.
<br>
By default, the text in <b>&lt;th&gt;</b> elements are bold and centered, but you can change that with CSS.
