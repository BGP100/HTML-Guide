<a href="https://github.com/BGP100/topnav.html">Click Here</a> to see the code for the <b>Navigation Var</b>.
<hr>
<b>Vertical:</b>
<br>
<img src="https://i.imgur.com/28C5TKf.png">
<br>
<b>Horizontal:</b>
<br>
<img src="https://i.imgur.com/xLGioc3.png">
<br>
<img src="https://i.imgur.com/CaapVo5.png">
<hr>
Having easy-to-use navigation is important for any web site.
<br>
With CSS you can transform boring HTML menus into good-looking navigation bars.
<h1>Navigation Bar = List of Links</h1>
A navigation bar needs standard HTML as a base.
<br>
In our examples we will build the navigation bar from a standard HTML list.
<br>
A navigation bar is basically a list of links, so using the <b>&lt;ul&gt;</b> and <b>&lt;li&gt;</b> elements makes perfect sense:
<pre>
&lt;ul&gt;
  &lt;li&gt;&lt;a href="default.asp"&gt;Home&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="news.asp"&gt;News&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="contact.asp"&gt;Contact&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="about.asp"&gt;About&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
</pre>
Now let's remove the bullets and the margins and padding from the list:
<pre>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
</pre>
<b>Explained:</b>
<ul>
  <li><b>list-style-type: none;</b> - Removes the bullets. A navigation bar does not need list markers</li>
  <li>Set <b>margin: 0;</b> and <b>padding: 0;</b> to remove browser default settings</li>
</ul>
The code in the example above is the standard code used in both vertical, and horizontal navigation bars, which you will learn more about in the next chapters.
