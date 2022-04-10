<a href="/CSS/Advanced/TextEffects.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Advanced/2D-Transforms.md">Next &gt;</a>
<hr>
Web fonts allow Web designers to use fonts that are not installed on the user's computer.
<br>
When you have found/bought the font you wish to use, just include the font file on your web server, and it will be automatically downloaded to the user when needed.
<br>
Your "own" fonts are defined within the CSS <b>@font-face</b> rule.
<h1>Different Font Formats</h1>
<ul>
  <li><b>TrueType Fonts (TTF)</b></li>
</ul>
TrueType is a font standard developed in the late 1980s, by Apple and Microsoft. TrueType is the most common font format for both the Mac OS and Microsoft Windows operating systems.
<ul>
  <li><b>OpenType Fonts (OTF)</b></li>
</ul>
OpenType is a format for scalable computer fonts. It was built on TrueType, and is a registered trademark of Microsoft. OpenType fonts are used commonly today on the major computer platforms
<ul>
  <li><b>The Web Open Font Format (WOFF)</b></li>
</ul>

WOFF is a font format for use in web pages. It was developed in 2009, and is now a W3C Recommendation. WOFF is essentially OpenType or TrueType with compression and additional metadata. The goal is to support font distribution from a server to a client over a network with bandwidth constraints.
<ul>
  <li><b>The Web Open Font Format 2.0 (WOFF2)</b></li>
</ul>
TrueType/OpenType font that provides better compression than WOFF 1.0.
<ul>
  <li><b>SVG Fonts/Shapes</b></li>
</ul>
SVG fonts allow SVG to be used as glyphs when displaying text. The SVG 1.1 specification define a font module that allows the creation of fonts within an SVG document. You can also apply CSS to SVG documents, and the @font-face rule can be applied to text in SVG documents.
<ul>
  <li><b>Embedded OpenType Fonts (EOT)</b></li>
</ul>
EOT fonts are a compact form of OpenType fonts designed by Microsoft for use as embedded fonts on web pages.
<h1>Browser Support</h1>
The numbers in the table specifies the first browser version that fully supports the font format.
<table>
  <tr>
    <th>Format</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>TTF/OTF</td>
    <td>4.0</td>
    <td>9.0<code>*</code></td>
    <td>3.5</td>
    <td>3.1</td>
    <td>10.0</td>
  </tr>
  <tr>
    <td>WOFF</td>
    <td>5.0</td>
    <td>9.0</td>
    <td>3.6</td>
    <td>5.1</td>
    <td>11.1</td>
  </tr>
  <tr>
    <td>WOFF2</td>
    <td>36.0</td>
    <td>14.0</td>
    <td>39.0</td>
    <td>10.0</td>
    <td>26.0</td>
  </tr>
  <tr>
    <td>SVG</td>
    <td>Not Supported</td>
    <td>Not Supported</td>
    <td>Not Supported</td>
    <td>3.2</td>
    <td>Not Supported</td>
  </tr>
  <tr>
    <td>EOT</td>
    <td>Not Supported</td>
    <td>6.0</td>
    <td>Not Supported</td>
    <td>Not Supported</td>
    <td>Not Supported</td>
  </tr>
</table>
<code>*</code> The font format only works when set to be "installable".
<h1>Using the Font</h1>
In the <b>@font-face</b> rule; first define a name for the font (e.g. myFirstFont) and then point to the font file.
<br>
To use the font for an HTML element, refer to the name of the font (myFirstFont) through the <b>@font-family</b> property:
<pre>
@font-face {
  font-family: myFirstFont;
  src: url(sansation_light.woff);
}
div {
  font-family: myFirstFont;
}
</pre>
<h1>Bold Text</h1>
You must add another <b>@font-face</b> rule containing descriptors for bold text:
<pre>
@font-face {
  font-family: myFirstFont;
  src: url(sansation_bold.woff);
  font-weight: bold;
}
</pre>
The file "sansation_bold.woff" is another font file, that contains the bold characters for the Sansation font.
<br>
Browsers will use this whenever a piece of text with the font-family "myFirstFont" should render as bold.
<br>
This way you can have many <b>@font-face</b> rules for the same font.
