<h1>&lt;defs&gt; and &lt;filter&gt;</h1>
All internet SVG filters are defined within a <b>&lt;defs&gt;</b> element. The <b>&lt;defs&gt;</b> element is short for definitions and contains definition of special elements (such as filters).
<br>
The <b>&lt;filter&gt;</b> element is used to define an SVG filter. The <b>&lt;filter&gt;</b> element has a required id attribute which identifies the filter. The graphic then points to the filter to use.
<h1>&lt;feGaussianBlur&gt;</h1>
<img src="https://i.imgur.com/qZgtGlL.jpg" width="110" height="110">
<pre>&lt;svg height="110" width="110"&gt;&lt;defs&gt;&lt;filter id="f1" x="0" y="0"&gt;&lt;feGaussianBlur in="SourceGraphic" stdDeviation="15" /&gt;&lt;/filter&gt;&lt;/defs&gt;&lt;rect width="90" height="90" stroke="green" stroke-width="3" fill="yellow" filter="url(#f1)" /&gt;&lt;/svg&gt;</pre>
<b>Explanation:</b>
<ul>
  <li>The id attribute of the <b>&lt;filter&gt;</b> element defines a unique name for the filter.</li>
  <li>The blur effect is defined with the <b>&lt;feGaussianBlur&gt;</b> element.</li>
  <li>The in="<i>SourceGraphic</i>" part defines that the effect is created for the entire element.</li>
  <li>The stdDeviation attribute defines the amount of the blur.</li>
  <li>The filter attribute of the <b>&lt;rect&gt;</b> element links the element to the "<var>f1</var>" filter.</li>
</ul>
