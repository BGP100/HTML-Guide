<a href="/HTML/Symbols.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Charset.md">Next &gt;</a>
<hr>
Emojis are characters from the UTF-8 character set: 😄 😍 💗
<h1>What are they?</h1>
Emojis look like images, or icons, but they are not.
<br>
They are letters (characters) from the UTF-8 (Unicode) character set.
<h1>charset</h1>
To display an HTML page correctly, a web browser must know the character set used in the page.
<br>
This is specified in the &lt;meta&gt; tag:
<pre>&lt;meta charset="UTF-8"&gt;</pre>
<h1>UTF-8 Characters</h1>
Many UTF-8 characters cannot be typed on a keyboard, but they can always be displayed using numbers (called entity numbers):
<ul>
  <li>A is 65</li>
  <li>B is 66</li>
  <li>C is 67</li>
</ul>
<pre>
&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;meta charset=&quot;UTF-8&quot;&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;p&gt;I will display A B C&lt;/p&gt;
    &lt;p&gt;I will display &amp;#65; &amp;#66; &amp;#67;&lt;/p&gt;
  &lt;/body&gt;
&lt;/html&gt;
</pre>
The &lt;meta charset="UTF-8"&gt; element defines the character set.
<br>
The characters A, B, and C, are displayed by the numbers 65, 66, and 67.
<br>
To let the browser understand that you are displaying a character, you must start the entity number with &# and end it with ; (semicolon).
<h1>Emoji Characters</h1>
Emojis are also characters from the UTF-8 alphabet:
<ul>
  <li>😄 is 128516</li>
  <li>😍 is 128525</li>
  <li>💗 is 128151</li>
</ul>
<pre>
&lt;h1&gt;My First Emoji&lt;/h1&gt;
&lt;p&gt;&amp;#128512;&lt;/p&gt;
</pre>
Since Emojis are characters, they can be copied, displayed, and sized just like any other character in HTML.
<pre>
&lt;h1&gt;Sized Emojis&lt;/h1&gt;
&lt;p style="font-size:48px"&gt;&amp;#128512; &amp;#128516; &amp;#128525; &amp;#128151;&lt;/p&gt;
</pre>
<h1>Some Emojis</h1>
<table class="ws-table-all">
  <tr>
    <th>Emoji</th>
    <th>Value</th>
  </tr>
  <tr>
    <td>&#128507;</td>
    <td>&amp;#128507;</td>
  </tr>
  <tr>
    <td>&#128508;</td>
    <td>&amp;#128508;</td>
  </tr>
  <tr>
    <td>&#128509;</td>
    <td>&amp;#128509;</td>
  </tr>
  <tr>
    <td>&#128510;</td>
    <td>&amp;#128510;</td>
  </tr>
  <tr>
    <td>&#128511;</td>
    <td>&amp;#128511;</td>
  </tr>
  <tr>
    <td>&#128512;</td>
    <td>&amp;#128512;</td>
  </tr>
  <tr>
    <td>&#128513;</td>
    <td>&amp;#128513;</td>
  </tr>
  <tr>
    <td>&#128514;</td>
    <td>&amp;#128514;</td>
  </tr>
  <tr>
    <td>&#128515;</td>
    <td>&amp;#128515;</td>
  </tr>
  <tr>
    <td>&#128516;</td>
    <td>&amp;#128516;</td>
  </tr>
  <tr>
    <td>&#128517;</td>
    <td>&amp;#128517;</td>
  </tr>
</table>
