<a href="/HTML/Responsive.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Semantic.md">Next &gt;</a>
<hr>
HTML contains several elements for defining user input and computer code.
<pre>
&lt;code&gt;
x = 5;
y = 6;
z = x + y;
&lt;/code&gt;
</pre>
<h1>kbd</h1>
The HTML <b>&lt;kbd&gt;</b> element is used to define keyboard input. The content inside is displayed in the browser's default monospace font.
<pre>&lt;p&gt;Save the document by pressing &lt;kbd&gt;Ctrl + S&lt;/kbd&gt;&lt;/p&gt;</pre>
Save the document by pressing <kbd>Ctrl + S</kbd>
<br>
Some other times looks like this:
<img src="https://i.imgur.com/DdhiYbG.jpg" width="10%">
<h1>samp</h1>
The HTML <b>&lt;samp&gt;</b> element is used to define sample output from a computer program. The content inside is displayed in the browser's default monospace font.
<pre>
&lt;p&gt;Message from my computer:&lt;/p&gt;
&lt;p&lt;samp&gt;File not found.&lt;br&gt;Press F1 to continue&lt;/samp&gt;&lt;/p&gt;
</pre>
Message from my computer:
<p></p>
<samp>
File not found.
<br>
Press F1 to continue
</samp>
<h1>code</h1>
The HTML <b>&lt;code&gt;</b> element  is used to define a piece of computer code. The content inside is displayed in the browser's default monospace font.
<pre>
&lt;code&gt;
x = 5;
y = 6;
z = x + y;
&lt;/code&gt;
</pre>
<code>x = 5; y = 6; z = x + y;</code>
<p></p>
Notice that the <b>&lt;code&gt;</b> element does not preserve extra whitespace and line-breaks.
<br>
To fix this, you can put the <b>&lt;code&gt;</b> element inside a <b>&lt;pre&gt;</b> element:
<pre>
&lt;pre&gt;
&lt;code&gt;
x = 5;
y = 6;
z = x + y;
&lt;/code&gt;
&lt;/pre&gt;
</pre>
<pre>
<code>
x = 5;
y = 6;
z = x + y;
</code>
</pre>
<h1>var</h1>
The HTML <b>&lt;var&gt;</b> element  is used to define a variable in programming or in a mathematical expression. The content inside is typically displayed in italic.
<pre>&lt;p&gt;The area of a triangle is: 1/2 x &lt;var&gt;b&lt;/var&gt; x &lt;var&gt;h&lt;/var&gt;, where &lt;var&gt;b&lt;/var&gt; is the base, and &lt;var&gt;h&lt;/var&gt; is the vertical height.&lt;/p&gt;</pre>
The area of a triangle is: 1/2 x <i>b</i> x <i>h</i>, where <i>b</i> is the base, and <i>h</i> is the vertical height.
