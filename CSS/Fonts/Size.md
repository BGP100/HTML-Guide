<a href="/CSS/Fonts/Style.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Fonts/Google.md">Next &gt;</a>
<hr>
The <b>font-size</b> property sets the size of the text.
<br>
Being able to manage the text size is important in web design. However, you should not use font size adjustments to make paragraphs look like headings, or headings look like paragraphs.
<br>
Always use the proper HTML tags, like <b>&lt;h1&gt; ••• &lt;h6&gt;</b> for headings and <b>&lt;p&gt;</b> for paragraphs.
<br>
The font-size value can be an absolute, or relative size.
<br>
<b>Absolute size:</b>
<ul>
  <li>Sets the text to a specified size</li>
  <li>Does not allow a user to change the text size in all browsers (bad for accessibility reasons)</li>
  <li>Absolute size is useful when the physical size of the output is known</li>
</ul>
<b>Relative size:</b>
<ul>
  <li>Sets the size relative to surrounding elements</li>
  <li>Allows a user to change the text size in browsers</li>
</ul>
<h1>Size with Pixels</h1>
Setting the text size with pixels gives you full control over the text size:
<pre>
h1 {
  font-size: 40px;
}
h2 {
  font-size: 30px;
}
p {
  font-size: 14px;
}
</pre>
<h1>Size with em</h1>
To allow users to resize the text (in the browser menu), many developers use em instead of pixels.
<br>
1em is equal to the current font size. The default text size in browsers is 16px. So, the default size of 1em is 16px.
<br>
The size can be calculated from pixels to em using this formula: <i>pixels/16=em</i>
<pre>
h1 {
  font-size: 2.5em; /* 40px/16=2.5em */
}
h2 {
  font-size: 1.875em; /* 30px/16=1.875em */
}
p {
  font-size: 0.875em; /* 14px/16=0.875em */
}
</pre>
In the example above, the text size in em is the same as the previous example in pixels. However, with the em size, it is possible to adjust the text size in all browsers.
<br>
Unfortunately, there is still a problem with older versions of Internet Explorer. The text becomes larger than it should when made larger, and smaller than it should when made smaller.
<h1>Combination</h1>
The solution that works in all browsers, is to set a default font-size in percent for the <b>&lt;body&gt;</b> element:
<pre>
body {
  font-size: 100%;
}
h1 {
  font-size: 2.5em;
}
h2 {
  font-size: 1.875em;
}
p {
  font-size: 0.875em;
}
</pre>
<h1>Responsive</h1>
The text size can be set with a "vw" unit, which means the "viewport width".
<br>
That way the text size will follow the size of the browser window:
<br>
<img src="https://i.imgur.com/qXBUj73.jpg" width="70%">
<pre>&lt;h1 style="font-size:10vw"&gt;Hello World&lt;/h1&gt;</pre>
