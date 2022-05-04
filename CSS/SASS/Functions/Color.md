<a href="/CSS/SASS/Function/Introspetion.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="https://bledy-guides.repl.co/#sass">Next &gt;</a>
<hr>
We have divided the color functions in SASS into three parts: Set color functions, Get color functions, and Manipulate color functions:
1. Set Color Functions
<table class="ws-table-all notranslate">
  <tr>
    <th>Function</th>
    <th>Description &amp; Example</th>
  </tr>
  <tr>
    <td>rgb(<em>red</em>, <em>green</em>, <em>blue</em>)</td>
    <td>Sets a color using the Red-Green-Blue (RGB) model. An RGB color value is 
    specified with: rgb(red, green, blue). Each parameter defines the intensity 
    of that color and can be an integer between 0 and 255, or a percentage value 
    (from 0% to 100%).<br><br>
    <strong>Example:</strong><br>rgb(0, 0, 255); // rendered as blue because the 
    blue parameter is set to its highest value (255) and the others are set to 0</td>
  </tr>
  <tr>
    <td>rgba(<em>red</em>, <em>green</em>, <em>blue</em>, <em>alpha</em>)</td>
    <td>Sets a color using the Red-Green-Blue-Alpha (RGBA) model. RGBA color 
    values are an extension of RGB color values with an alpha channel - which 
    specifies the opacity of the color. The alpha parameter is a number between 
    0.0 (fully transparent) and 1.0 (fully opaque).<br><br>
    <strong>Example:</strong><br>rgba(0, 0, 255, 0.3); // rendered as blue with 
    opacity</td>
  </tr>
  <tr>
    <td>hsl(<em>hue</em>, <em>saturation</em>, <em>lightness</em>)</td>
    <td>Sets a color using the Hue-Saturation-Lightness (HSL) model - and 
    represents a cylindrical-coordinate representation of colors. Hue is a 
    degree on the color wheel (from 0 to 360) - 0 or 360 is red, 120 is green, 
    240 is blue. Saturation is a percentage value; 0% means a shade of gray and 
    100% is the full color. Lightness is also a percentage; 0% is black, 100% is 
    white.<br><br>
    <strong>Example:</strong><br>hsl(120, 100%, 50%); // green<br>hsl(120, 100%, 
    75%); // light green<br>hsl(120, 100%, 25%); // dark green<br>hsl(120, 60%, 
    70%); // pastel green <br></td>
  </tr>
  <tr>
    <td>hsla(<em>hue</em>, <em>saturation</em>, <em>lightness</em>, <em>alpha</em>)</td>
    <td>Sets a color using the Hue-Saturation-Lightness-Alpha (HSLA) model. HSLA 
    color values are an extension of HSL color values with an alpha channel - 
    which specifies the opacity of the color. The alpha parameter is a number 
    between 0.0 (fully transparent) and 1.0 (fully opaque).<br><br>
    <strong>Example:</strong><br>hsl(120, 100%, 50%, 0.3); // green with opacity<br>
    hsl(120, 100%, 75%, 0.3); // light green with opacity</td>
  </tr>
  <tr>
    <td>grayscale(<em>color</em>)</td>
    <td>Sets a gray color with the same lightness as <em>color</em>.<br><br>
    <strong>Example:</strong><br>grayscale(#7fffd4);<br>Result: #c6c6c6</td>
  </tr>
  <tr>
    <td>complement(<em>color</em>)</td>
    <td>Sets a color that is the complementary color of <em>color</em>.<br><br>
    <strong>Example:</strong><br>complement(#7fffd4);<br>Result: #ff7faa</td>
  </tr>
  <tr>
    <td>invert(<em>color</em>, <em>weight</em>)</td>
    <td>Sets a color that is the inverse or negative color of <em>color</em>. 
    The <em>weight</em> parameter is optional and must be a number between 0% 
    and 100%. Default is 100%.<br><br>
    <strong>Example:</strong><br>invert(white);<br>Result: black</td>
  </tr>
</table>
2. Get Color Function
<table class="ws-table-all notranslate">
  <tr>
    <th>Function</th>
    <th>Description &amp; Example</th>
  </tr>
  <tr>
    <td>red(<em>color</em>)</td>
    <td>Returns the red value of <em>color</em> as a number between 0 and 255.<br><br>
    <strong>Example:</strong><br>red(#7fffd4);<br>Result: 127<br>red(red);<br>Result: 
    255</td>
  </tr>
  <tr>
    <td>green(<em>color</em>)</td>
    <td>Returns the green value of <em>color</em> as a number between 0 and 255.<br><br>
    <strong>Example:</strong><br>green(#7fffd4);<br>Result: 255<br>green(blue);<br>Result: 
    0</td>
  </tr>
  <tr>
    <td>blue(<em>color</em>)</td>
    <td>Returns the blue value of <em>color</em> as a number between 0 and 255.<br><br>
    <strong>Example:</strong><br>blue(#7fffd4);<br>Result: 212<br>blue(blue);<br>Result: 255</td>
  </tr>
  <tr>
    <td>hue(<em>color</em>)</td>
    <td>Returns the hue of <em>color</em> as a number between 0deg and 360deg.<br><br>
    <strong>Example:</strong><br>hue(#7fffd4);<br>Result: 160deg</td>
  </tr>
  <tr>
    <td>saturation(<em>color</em>)</td>
    <td>Returns the HSL saturation of <em>color</em> as a number between 0% and 
    100%.<br><br>
    <strong>Example:</strong><br>saturation(#7fffd4);<br>Result: 100%</td>
  </tr>
  <tr>
    <td>lightness(<em>color</em>)</td>
    <td>Returns the HSL lightness of <em>color</em> as a number between 0% and 
    100%.<br><br>
    <strong>Example:</strong><br>lightness(#7fffd4);<br>Result: 74.9%</td>
  </tr>
  <tr>
    <td>alpha(<em>color</em>)</td>
    <td>Returns the alpha channel of <em>color</em> as a number between 0 and 1.<br><br>
    <strong>Example:</strong><br>alpha(#7fffd4);<br>Result: 1</td>
  </tr>
  <tr>
    <td>opacity(<em>color</em>)</td>
    <td>Returns the alpha channel of <em>color</em> as a number between 0 and 1.<br><br>
    <strong>Example:</strong><br>opacity(rgba(127, 255, 212, 0.5));<br>Result: 
    0.5</td>
  </tr>
</table>
3. Manipulate Color Functions
<table class="ws-table-all notranslate">
  <tr>
    <th>Function</th>
    <th>Description &amp; Example</th>
  </tr>
  <tr>
    <td>mix(<em>color1</em>, <em>color2</em>, <em>weight</em>)</td>
    <td>Creates a color that is a mix of <em>color1</em> and <em>color2</em>. 
    The <em>weight</em> parameter must be between 0% and 100%. A larger weight 
    means that more of color1 should be used. A smaller weight means that more 
    of color2 should be used. Default is 50%.</td>
  </tr>
  <tr>
    <td>adjust-hue(<em>color</em>, <em>degrees</em>)</td>
    <td>Adjusts the <em>color</em>'s hue with a degree from -360deg to 360deg.<br><br>
    <strong>Example:</strong><br>adjust-hue(#7fffd4, 80deg);<br>Result: #8080ff</td>
  </tr>
  <tr>
    <td>adjust-color(<em>color</em>, <em>red</em>, <em>green</em>, <em>blue</em>,
    <em>hue</em>, <em>saturation</em>, <em>lightness</em>, <em>alpha</em>)</td>
    <td>Adjusts one or more parameters by the specified amount. This function 
    adds or subtracts the specified amount to/from the existing color value.<br>
    <br>
    <strong>Example:</strong><br>adjust-color(#7fffd4, blue: 25);<br>Result:</td>
  </tr>
  <tr>
    <td>change-color(<em>color</em>, <em>red</em>, <em>green</em>, <em>blue</em>,
    <em>hue</em>, <em>saturation</em>, <em>lightness</em>, <em>alpha</em>)</td>
    <td>Sets one or more parameters of a <em>color</em> to new values.<br><br>
    <strong>Example:</strong><br>change-color(#7fffd4, red: 255);<br>Result: 
    #ffffd4</td>
  </tr>
  <tr>
    <td>scale-color(<em>color</em>, <em>red</em>, <em>green</em>, <em>blue</em>,&nbsp;
    <em>saturation</em>, <em>lightness</em>, <em>alpha</em>)</td>
    <td>Scales one or more parameters of <em>color</em>.</td>
  </tr>
  <tr>
    <td>rgba(<em>color</em>, <em>alpha</em>)</td>
    <td>Creates a new color of <em>color</em> with the given <em>alpha</em> 
    channel.<br><br><strong>Example:</strong><br>rgba(#7fffd4, 30%);<br>Result: 
    rgba(127, 255, 212, 0.3)</td>
  </tr>
  <tr>
    <td>lighten(<em>color</em>, <em>amount</em>)</td>
    <td>Creates a lighter color of <em>color</em> with an <em>amount</em> 
    between 0% and 100%. The amount parameter increases the HSL lightness by 
    that percent.</td>
  </tr>
  <tr>
    <td>darken(<em>color</em>, <em>amount</em>)</td>
    <td>Creates a darker color of <em>color</em> with an <em>amount</em> between 
    0% and 100%. The amount parameter decreases the HSL lightness by that 
    percent.</td>
  </tr>
  <tr>
    <td>saturate(<em>color</em>, <em>amount</em>)</td>
    <td>Creates a more saturated color of <em>color</em> with an <em>amount</em> 
    between 0% and 100%. The amount parameter increases the HSL saturation by 
    that percent.</td>
  </tr>
  <tr>
    <td>desaturate(<em>color</em>, <em>amount</em>)</td>
    <td>Creates a less saturated color of <em>color</em> with an <em>amount</em> 
    between 0% and 100%. The amount parameter decreases the HSL saturation by 
    that percent.</td>
  </tr>
  <tr>
    <td>opacify(<em>color</em>, <em>amount</em>)</td>
    <td>Creates a more opaque color of <em>color</em> with an <em>amount</em> 
    between 0 and 1. The amount parameter increases the alpha channel by that 
    amount.</td>
  </tr>
  <tr>
    <td>fade-in(<em>color</em>, <em>amount</em>)</td>
    <td>Creates a more opaque color of <em>color</em> with an <em>amount</em> 
    between 0 and 1. The amount parameter increases the alpha channel by that 
    amount.</td>
  </tr>
  <tr>
    <td>transparentize(<em>color</em>, <em>amount</em>)</td>
    <td>Creates a more transparent color of <em>color</em> with an <em>amount</em> 
    between 0 and 1. The amount parameter decreases the alpha channel by that 
    amount.</td>
  </tr>
  <tr>
    <td>fade-out(<em>color</em>, <em>amount</em>)</td>
    <td>Creates a more transparent color of <em>color</em> with an <em>amount</em> 
    between 0 and 1. The amount parameter decreases the alpha channel by that 
    amount.</td>
  </tr>
</table>
