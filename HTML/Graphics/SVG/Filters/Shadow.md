<h1>&lt;defs&gt; and &lt;filter&gt;</h1>
All internet SVG filters are defined within a <b>&lt;defs&gt;</b> element. The <b>&lt;defs&gt;</b> element is short for definitions and contains definition of special elements (such as filters).
<br>
The <b>&lt;filter&gt;</b> element is used to define an SVG filter. The <b>&lt;filter&gt;</b> element has a required id attribute which identifies the filter. The graphic then points to the filter to use.
<h1>&lt;feOffset&gt;</h1>
<h1>Example 1</h1>
<img src="https://i.imgur.com/tXZVQzz.jpg" width="120" height="120">
<pre>&lt;svg height="120" width="120"&gt;&lt;defs&gt;&lt;filter id="f1" x="0" y="0" width="200%" height="200%"&gt;&lt;feOffset result="offOut" in="SourceGraphic" dx="20" dy="20" /&gt;&lt;feBlend in="SourceGraphic" in2="offOut" mode="normal" /&gt;&lt;/filter&gt;&lt;/defs&gt;&lt;rect width="90" height="90" stroke="green" stroke-width="3" fill="yellow" filter="url(#f1)" /&gt;&lt;/svg&gt;</pre>
<b>Explanation:</b>
<ul>
  <li>The id attribute of the <b>&lt;filter&gt;</b> element defines a unique name for the filter</li>
  <li>The filter attribute of the <b>&lt;rect&gt;</b> element links the element to the "<i>f1</i>" filter</li>
</ul>
<h1>Example 2</h1>
<img src="https://i.imgur.com/QbGpiiH.jpg" width="120" height="120">
<pre>&lt;svg height="120" width="120"&gt;&lt;defs&gt;&lt;filter id="f2" x="0" y="0" width="200%" height="200%"&gt;&lt;feOffset result="offOut" in="SourceGraphic" dx="20" dy="20" /&gt;&lt;feGaussianBlur result="blurOut" in="offOut" stdDeviation="10" /&gt;&lt;feBlend in="SourceGraphic" in2="blurOut" mode="normal" /&gt;&lt;/filter&gt;&lt;/defs&gt;&lt;rect width="90" height="90" stroke="green" stroke-width="3" fill="yellow" filter="url(#f2)" /&gt;&lt;/svg&gt;</pre>
<b>Explanation:</b>
<ul>
  <li>The stdDeviation attribute of the <b>&lt;feGaussianBlur&gt;</b> element defines the amount of the blur.</li>
</ul>
<h1>Example 3</h1>
<img src="https://i.imgur.com/cNbwjIv.jpg" width="120" height="120">
<pre>&lt;svg height="120" width="120"&gt;&lt;defs&gt;&lt;filter id="f3" x="0" y="0" width="200%" height="200%"&gt;&lt;feOffset result="offOut" in="SourceAlpha" dx="20" dy="20" /&gt;&lt;feGaussianBlur result="blurOut" in="offOut" stdDeviation="10" /&gt;&lt;feBlend in="SourceGraphic" in2="blurOut" mode="normal" /&gt;&lt;/filter&gt;&lt;/defs&gt;&lt;rect width="90" height="90" stroke="green" stroke-width="3" fill="yellow" filter="url(#f3)" /&gt;&lt;/svg&gt;</pre>
<b>Explanation:</b>
<ul>
  <li>The in attribute of the <b>&lt;feOffset&gt;</b> element is changed to "SourceAlpha" which uses the Alpha channel for the blur instead of the entire RGBA pixel.</li>
</ul>
<h1>Example 4</h1>
<img src="https://i.imgur.com/LKP96Vn.jpg" width="120" height="120">
<pre>&lt;svg height="120" width="120"&gt;&lt;defs&gt;&lt;filter id="f4" x="0" y="0" width="200%" height="200%"&gt;&lt;feOffset result="offOut" in="SourceGraphic" dx="20" dy="20" /&gt;&lt;feColorMatrix result="matrixOut" in="offOut" type="matrix" values="0.2 0 0 0 0 0 0.2 0 0 0 0 0 0.2 0 0 0 0 0 1 0" /&gt;&lt;feGaussianBlur result="blurOut" in="matrixOut" stdDeviation="10" /&gt;&lt;feBlend in="SourceGraphic" in2="blurOut" mode="normal" /&gt;&lt;/filter&gt;&lt;/defs&gt;&lt;rect width="90" height="90" stroke="green" stroke-width="3" fill="yellow" filter="url(#f4)" /&gt;&lt;/svg&gt;</pre>
<b>Explanation:</b>
<ul>
  <li>The <b>&lt;feColorMatrix&gt;</b> filter is used to transform the colors in the offset image closer to black. The three values of '<var>0.2</var>' in the matrix all get multiplied by the red, green and blue channels. Reducing their values brings the colors closer to black (black is 0)</li>
</ul>
