If you do not want to use any of the standard fonts in HTML, you can use Google Fonts.
<br>
Google Fonts are free to use, and have more than 1000 fonts to choose from.
<h1>How to use'em?</h1>
Just add a special style sheet link in the <b>&lt;head&gt;</b> section and then refer to the font in the CSS.
<pre>
&lt;link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Sofia"&gt;
&lt;style&gt;
body {
  font-family: "Sofia", sans-serif;
}
&lt;/style&gt;
</pre>
<img src="https://i.imgur.com/HExD1WH.jpg" width="50%">
<p></p>
<pre>
&lt;link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Trirong"&gt;
&lt;style&gt;
body {
  font-family: "Trirong", serif;
}
&lt;/style&gt;
</pre>
<img src="https://i.imgur.com/y8BqREx.jpg" width="50%">
<p></p>
<pre>
&lt;link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Audiowide"&gt;
&lt;style&gt;
body {
  font-family: "Audiowide", sans-serif;
}
&lt;/style&gt;
</pre>
<img src="https://i.imgur.com/tdTammj.jpg" width="50%">
<h1>Multiple</h1>
To use multiple Google fonts, just separate the font names with a pipe character (<b>|</b>), like this:
<pre>
&lt;link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Audiowide|Sofia|Trirong"&gt;
&lt;style&gt;
h1.a {font-family: "Audiowide", sans-serif;}
h1.b {font-family: "Sofia", sans-serif;}
h1.c {font-family: "Trirong", serif;}
&lt;/style&gt;
</pre>
