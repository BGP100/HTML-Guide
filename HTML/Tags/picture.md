The <b>&lt;picture&gt;</b> tag gives web developers more flexibility in specifying image resources.
<br>
The most common use of the <b>&lt;picture&gt;</b> element will be for art direction in responsive designs. Instead of having one image that is scaled up or down based on the viewport width, multiple images can be designed to more nicely fill the browser viewport.
<br>
The <b>&lt;picture&gt;</b> element contains two tags: one or more <a href="source.md">&lt;source&gt;</a> tags and one <a href="img.md">&lt;img&gt;</a> tag.
<br>
The browser will look for the first <a href="source.md">&lt;source&gt;</a> element where the media query matches the current viewport width, and then it will display the proper image (specified in the srcset attribute). The <a href=".md">&lt;img&gt;</a> element is required as the last child of the <b>&lt;picture&gt;</b> element, as a fallback option if none of the source tags matches.
<br>
<b><i>Tip:</i></b> The <b>&lt;picture&gt;</b> element works "similar" to <a href="video.md">&lt;video&gt;</a> and <a href="audio.md">&lt;audio&gt;</a>. You set up different sources, and the first source that fits the preferences is the one being used.
<pre>
&lt;picture&gt;
  &lt;source media="(min-width:650px)" srcset="img_pink_flowers.jpg"&gt;
  &lt;source media="(min-width:465px)" srcset="img_white_flower.jpg"&gt;
  &lt;img src="img_orange_flowers.jpg" alt="Flowers" style="width:auto;"&gt;
&lt;/picture&gt;
</pre>
<h1>Browser Support</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>Browser</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>Version</td>
    <td>38.0</td>
    <td>13.0</td>
    <td>38.0</td>
    <td>9.1</td>
    <td>25.0</td>
  </tr>
</table>
<h1>Standard</h1>
The <b>&lt;picture&gt;</b> tag supports the standard attributes.
<h1>Event</h1>
The <b>&lt;picture&gt;</b> tag supports the event attributes.
