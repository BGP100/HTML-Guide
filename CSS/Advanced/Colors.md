CSS supports 140+ color names, HEX values, RGB values, RGBA values, HSL values, HSLA values, and opacity. <a href="/CSS/ColorsList/">List of Colors</a>
<h1>RGBA</h1>
RGBA color values are an extension of RGB color values with an alpha channel - which specifies the opacity for a color.
<br>
An RGBA color value is specified with: rgba(red, green, blue, alpha). The alpha parameter is a number between 0.0 (fully transparent) and 1.0 (fully opaque).
<br>
<img src="https://i.imgur.com/eqWoFIS.png" width="100%">
<br>
The following example defines different RGBA colors:
<pre>
#p1{background-color:rgba(255,0,0,0.3);} /* red with opacity */
#p2{background-color:rgba(0,255,0,0.3);} /* green with opacity */
#p3{background-color:rgba(0,0,255,0.3);} /* blue with opacity */
</pre>
<h1>HSL</h1>
HSL stands for Hue, Saturation and Lightness.
<br>
An HSL color value is specified with: hsl(hue, saturation, lightness).
<ul>
  <li>Hue is a degree on the color wheel (from 0 to 360):</li>
  <ul>
    <li>0 (or 360) is red</li>
    <li>120 is green</li>
    <li>240 is blue</li>
  </ul>
  <li>Saturation is a percentage value: 100% is the full color.</li>
  <li>Lightness is also a percentage; 0% is dark (black) and 100% is white.</li>
</ul>
<img src="https://i.imgur.com/qcJYO4z.png" width="100%">
<br>
The following example defines different HSL colors:
<pre>
#p1{background-color:hsl(120,100%,50%);} /* green */
#p2{background-color:hsl(120,100%,75%);} /* light green */
#p3{background-color:hsl(120,100%,25%);} /* dark green */
#p4{background-color:hsl(120,60%,70%);} /* pastel green */
</pre>
<h1>HSLA</h1>
HSLA color values are an extension of HSL color values with an alpha channel - which specifies the opacity for a color.
<br>
An HSLA color value is specified with: hsla(hue, saturation, lightness, alpha), where the alpha parameter defines the opacity. The alpha parameter is a number between 0.0 (fully transparent) and 1.0 (fully opaque).
<br>
<img src="https://i.imgur.com/CgDnwjv.png" width="100%">
<br>
The following example defines different HSLA colors:
<pre>
#p1{background-color:hsla(120,100%,50%,0.3);} /* green with opacity */
#p2{background-color:hsla(120,100%,75%,0.3);} /* light green with opacity */
#p3{background-color:hsla(120,100%,25%,0.3);} /* dark green with opacity */
#p4{background-color:hsla(120,60%,70%,0.3);} /* pastel green with opacity */
</pre>
<h1>Opacity</h1>
The CSS opacity property sets the opacity for the whole element (both background color and text will be opaque/transparent).
<br>
The opacity property value must be a number between 0.0 (fully transparent) and 1.0 (fully opaque).
<br>
<img src="https://i.imgur.com/Niq21NI.png">
<br>
Notice that the text above will also be transparent/opaque!
<br>
The following example shows different elements with opacity:
<pre>
#p1{background-color:rgb(255,0,0);opacity:0.6;} /* red with opacity */
#p2{background-color:rgb(0,255,0);opacity:0.6;} /* green with opacity */
#p3{background-color:rgb(0,0,255);opacity:0.6;} /* blue with opacity */
</pre>
