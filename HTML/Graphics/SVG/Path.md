<a href="/HTML/Graphics/SVG/Polyline.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Graphics/SVG/Text.md">Next &gt;</a>
<hr>
The &lt;path&gt; element is used to define a path.
<br>
The following commands are available for path data:
<ul>
  <li>M = moveto</li>
  <li>L = lineto</li>
  <li>H = horizontal lineto</li>
  <li>V = vertical lineto</li>
  <li>C = curveto</li>
  <li>S = smooth curveto</li>
  <li>Q = quadratic Bézier curve</li>
  <li>T = smooth quadratic Bézier curveto</li>
  <li>A = elliptical Arc</li>
  <li>Z = closepath</li>
</ul>
<b>Note:</b> All of the commands above can also be expressed with lower letters. Capital letters means absolutely positioned, lower cases means relatively positioned.
<h1>Example 1</h1>
<img src="https://i.imgur.com/pAqURcI.png" height="200" width="150">
<pre>&lt;svg height="210" width="400"&gt;&lt;path d="M150 0 L75 200 L225 200 Z" /&gt;&lt;/svg&gt;</pre>
<h1>Example 2</h1>
<img src="https://i.imgur.com/VV25Hnb.png" height="396" width="362">
<pre>&lt;svg height="400" width="450"&gt;&lt;path id="lineAB" d="M 100 350 l 150 -300" stroke="red" stroke-width="3" fill="none" /&gt;&lt;path id="lineBC" d="M 250 50 l 150 300" stroke="red" stroke-width="3" fill="none" /&gt;&lt;path d="M 175 200 l 150 0" stroke="green" stroke-width="3" fill="none" /&gt;&lt;path d="M 100 350 q 150 -300 300 0" stroke="blue" stroke-width="5" fill="none" /&gt;&lt;!-- Mark relevant points --&gt;&lt;g stroke="black" stroke-width="3" fill="black"&gt;&lt;circle id="pointA" cx="100" cy="350" r="3" /&gt;&lt;circle id="pointB" cx="250" cy="50" r="3" /&gt;&lt;circle id="pointC" cx="400" cy="350" r="3" /&gt;&lt;/g&gt;&lt;!-- Label the points --&gt;&lt;g font-size="30" font-family="sans-serif" fill="black" stroke="none" text-anchor="middle"&gt;&lt;text x="100" y="350" dx="-30"&gt;A&lt;/text&gt;&lt;text x="250" y="50" dy="-10"&gt;B&lt;/text&gt;&lt;text x="400" y="350" dx="30"&gt;C&lt;/text&gt;&lt;/g&gt;&lt;/svg&gt;</pre>
Complex? YES!!!! Because of the complexity involved in drawing paths it is highly recommended to use an SVG editor to create complex graphics.
