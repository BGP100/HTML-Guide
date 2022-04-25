<a href="/HTML/BeginnerGuide.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Symbols.md">Next &gt;</a>
<hr>
Reserved characters in HTML must be replaced with character entities.
<hr>
You will see more HTML symbols in the <a href="Symbols.md">symbols chapter.</a>
<hr>
Some characters are reserved in HTML.
<br>
If you use the less than (&lt;) or greater than (&gt;) signs in your text, the browser might mix them with tags.
<br>
Character entities are used to display reserved characters in HTML.
<br>
A character entity looks like this:
<pre>
&amp;entity_name;
-
OR
-
&amp;#entity_number;
</pre>
To display a less than sign (&lt;) we must write: &amp;lt; or &amp;#60;
<br>
To display a less than sign (&gt;) we must write: &amp;gt; or &amp;#62;
<h1>Non-breaking Space</h1>
A commonly used entity in HTML is the non-breaking space: &nbsp;
<br>
A non-breaking space is a space that will not break into a new line.
<br>
Two words separated by a non-breaking space will stick together (not break into a new line). This is handy when breaking the words might be disruptive.
<br>
Examples:
<ul>
  <li>§ 10</li>
  <li>10 km/hr</li>
  <li>10 PM</li>
</ul>
Another common use of the non-breaking space is to prevent browsers from truncating spaces in HTML pages.
<br>
If you write 10 spaces in your text, the browser will remove 9 of them. To add real spaces to your text, you can use the &amp;nbsp; character entity.
<h1>Some Useful Entities</h1>
<table>
  <tr>
    <th>Result</th>
    <th>Description</th>
    <th>Entity Name</th>
    <th>Entity Number</th>
  </tr>
  <tr>
    <td>&nbsp;</td>
    <td>non-breaking space</td>
    <td>&amp;nbsp;</td>
    <td>&amp;#160;</td>
  </tr>
  <tr>
    <td>&lt;</td>
    <td>less than</td>
    <td>&amp;lt;</td>
    <td>&amp;#60;</td>
  </tr>
  <tr>
    <td>&gt;</td>
    <td>greater than</td>
    <td>&amp;gt;</td>
    <td>&amp;#62;</td>
  </tr>
  <tr>
    <td>&amp;</td>
    <td>ampersand</td>
    <td>&amp;amp;</td>
    <td>&amp;#38;</td>
  </tr>
  <tr>
    <td>&quot;</td>
    <td>quotation mark</td>
    <td>&amp;quot;</td>
    <td>&amp;#34;</td>
  </tr>
  <tr>
    <td>&apos;</td>
    <td>apostrophe</td>
    <td>&amp;apos;</td>
    <td>&amp;#39;</td>
  </tr>
  <tr>
    <td>&cent;</td>
    <td>cent</td>
    <td>&amp;cent;</td>
    <td>&amp;#162;</td>
  </tr>
  <tr>
    <td>&pound;</td>
    <td>pound</td>
    <td>&amp;pound;</td>
    <td>&amp;#163;</td>
  </tr>
  <tr>
    <td>&yen;</td>
    <td>yen</td>
    <td>&amp;yen;</td>
    <td>&amp;#165;</td>
  </tr>
  <tr>
    <td>&euro;</td>
    <td>euro</td>
    <td>&amp;euro;</td>
    <td>&amp;#8364;</td>
  </tr>
  <tr>
    <td>&copy;</td>
    <td>copyright</td>
    <td>&amp;copy;</td>
    <td>&amp;#169;</td>
  </tr>
  <tr>
    <td>&reg;</td>
    <td>registered trademark</td>
    <td>&amp;reg;</td>
    <td>&amp;#174;</td>
  </tr>
</table>
<h1>Combining Marks</h1>
A diacritical mark is a "glyph" added to a letter.
<br>
Some diacritical marks, like grave (<code> ̀</code>) and acute (<code> ́</code>) are called accents.
<br>
Diacritical marks can appear both above and below a letter, inside a letter, and between two letters.
<br>
Diacritical marks can be used in combination with alphanumeric characters to produce a character that is not present in the character set (encoding) used in the page.
<br>
Here are some examples:
<table>
  <tr>
    <th>Mark</th>
    <th>Character</th>
    <th>Construct</th>
    <th>Result</th>
  </tr>
  <tr>
    <td>&#768;</td>
    <td>a</td>
    <td>a&amp;#768;</td>
    <td>a&#768;</td>
  </tr>
  <tr>
    <td>&#769;</td>
    <td>a</td>
    <td>a&amp;#769;</td>
    <td>a&#769;</td>
  </tr>
  <tr>
    <td>&#770;</td>
    <td>a</td>
    <td>a&amp;#770;</td>
    <td>a&#770;</td>
  </tr>
  <tr>
    <td>&#771;</td>
    <td>a</td>
    <td>a&amp;#771;</td>
    <td>a&#771;</td>
  </tr>
  <tr>
    <td>&#768;</td>
    <td>O</td>
    <td>O&amp;#768;</td>
    <td>O&#768;</td>
  </tr>
  <tr>
    <td>&#769;</td>
    <td>O</td>
    <td>O&amp;#769;</td>
    <td>O&#769;</td>
  </tr>
  <tr>
    <td>&#770;</td>
    <td>O</td>
    <td>O&amp;#770;</td>
    <td>O&#770;</td>
  </tr>
  <tr>
    <td>&#771;</td>
    <td>O</td>
    <td>O&amp;#771;</td>
    <td>O&#771;</td>
  </tr>
</table>
