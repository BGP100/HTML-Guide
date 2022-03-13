Choosing the right font for your website is important!
<h1>Why?</h1>
Choosing the right font has a huge impact on how the readers experience a website.
<br>
The right font can create a strong identity for your brand.
<br>
Using a font that is easy to read is important. The font adds value to your text. It is also important to choose the correct color and text size for the font.
<h1>Some Fonts</h1>
In CSS there are five generic font families:
<ul>
  <li>Serif fonts have a small stroke at the edges of each letter. They create a sense of formality and elegance.</li>
  <li>Sans-serif fonts have clean lines (no small strokes attached). They create a modern and minimalistic look.</li>
  <li>Monospace fonts - here all the letters have the same fixed width. They create a mechanical look.</li>
  <li>Cursive fonts imitate human handwriting.</li>
  <li>Fantasy fonts are decorative/playful fonts.</li>
</ul>
All the different font names belong to one of the generic font families.
<br>
<img src="https://i.imgur.com/GZEYbTy.gif">
<h1>Property</h1>
In CSS, we use the <b>font-family</b> property to specify the font of a text.
<br>
<b>Tip:</b> The <b>font-family</b> property should hold several font names as a "fallback" system, to ensure maximum compatibility between browsers/operating systems. Start with the font you want, and end with a generic family (to let the browser pick a similar font in the generic family, if no other fonts are available). The font names should be separated with comma. Read more about fallback fonts in the <a href="WebSafe.md">Web Safe chatper</a>.
<pre>
.ff1 {
  font-family: "Times New Roman", Times, serif;
}
.ff2 {
  font-family: Arial, Helvetica, sans-serif;
}
.ff3 {
  font-family: "Lucida Console", "Courier New", monospace;
}
</pre>
