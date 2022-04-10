<a href="/CSS/SASS/Variables.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/SASS/@/import.md">Next &gt;</a>
<hr>
Sass lets you nest CSS selectors in the same way as HTML.
<br>
Look at an example of some Sass code for a site's navigation:
<pre>
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }
  li {
    display: inline-block;
  }
  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
</pre>
Notice that in SASS, the <b>ul</b>, <b>li</b>, and <b>a</b> selectors are nested inside the <b>nav</b> selector.
<br>
While in CSS, the rules are defined one by one (not nested):
<pre>
nav ul {
  margin: 0;
  padding: 0;
  list-style: none;
}
nav li {
  display: inline-block;
}
nav a {
  display: block;
  padding: 6px 12px;
  text-decoration: none;
}
</pre>
Because you can nest properties in SASS, it is cleaner and easier to read than standard CSS.
<h1>Properties</h1>
Many CSS properties have the same prefix, like <b>font-family</b>, <b>font-size</b> and <b>font-weight</b> or <b>text-align</b>, <b>text-transform</b> and text-overflow.
<br>
With SASS you can write them as nested properties:
<pre>
font: {
  family: Helvetica, sans-serif;
  size: 18px;
  weight: bold;
}
text: {
  align: center;
  transform: lowercase;
  overflow: hidden;
}
</pre>
The SASS transpiler will convert the above to normal CSS:
<pre>
font-family: Helvetica, sans-serif;
font-size: 18px;
font-weight: bold;
text-align: center;
text-transform: lowercase;
text-overflow: hidden;
</pre>
