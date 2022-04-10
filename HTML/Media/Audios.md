<a href="/HTML/Media/Videos.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Media/Plug-ins.md">Next &gt;</a>
<hr>
The HTML <b>&lt;audio&gt;</b> element is used to play an audio file on a web page.
<h1>How it works</h1>
The controls attribute adds audio controls, like play, pause, and volume.
<br>
The <b>&lt;source&gt;</b> element allows you to specify alternative audio files which the browser may choose from. The browser will use the first recognized format.
<br>
The text between the <b>&lt;audio&gt;</b> and <b>&lt;/audio&gt;</b> tags will only be displayed in browsers that do not support the <b>&lt;audio&gt;</b> element.
<h1>The Element</h1>
To play an audio file in HTML, use the <b>&lt;audio&gt;</b> element:
<pre>
&lt;audio controls&gt;
  &lt;source src="horse.ogg" type="audio/ogg"&gt;
  &lt;source src="horse.mp3" type="audio/mpeg"&gt;
  Your browser does not support the audio element.
&lt;/audio&gt;
</pre>
<h1>autoplay</h1>
To start an audio file automatically, use the <b>autoplay</b> attribute:
<pre>
&lt;audio controls <b>autoplay</b>&gt;
  &lt;source src="horse.ogg" type="audio/ogg"&gt;
  &lt;source src="horse.mp3" type="audio/mpeg"&gt;
  Your browser does not support the audio element.
&lt;/audio&gt;
</pre>
Add <b>muted</b> after <b>autoplay</b> to let your audio file start playing automatically but muted:
<pre>
&lt;audio controls autoplay <b>muted</b>&gt;
  &lt;source src="horse.ogg" type="audio/ogg"&gt;
  &lt;source src="horse.mp3" type="audio/mpeg"&gt;
  Your browser does not support the audio element.
&lt;/audio&gt;
</pre>
<h1>Browser Support</h1>
The numbers in the table specify the first browser version that fully supports the <b>&lt;audio&gt;</b> element.
<table class="ws-table-all notranslate">
  <tr>
    <th>Browser</th>
    <td>Chrome</td>
    <td>Edge</td>
    <td>Firefox</td>
    <td>Safari</td>
    <td>Opera</td>
  </tr>
  <tr>
    <th>Version</th>
    <td>4.0</td>
    <td>9.0</td>
    <td>3.5</td>
    <td>4.0</td>
    <td>10.5</td>
  </tr>
</table>
<h1>Audio Formats</h1>
There are three supported audio formats: MP3, WAV, and OGG. The browser support for the different formats is:
<table class="ws-table-all notranslate">
  <tr>
    <th>Browser</th>
    <th>MP3</th>
    <th>WAV</th>
    <th>OGG</th>
  </tr>
  <tr>
    <td>Edge</td>
    <td>YES</td>
    <td>YES<code>*</code></td>
    <td>YES<code>*</code></td>
  </tr>
  <tr>
    <td>Chrome</td>
    <td>YES</td>
    <td>YES</td>
    <td>YES</td>
  </tr>
  <tr>
    <td>Firefox</td>
    <td>YES</td>
    <td>YES</td>
    <td>YES</td>
  </tr>
  <tr>
    <td>Safari</td>
    <td>YES</td>
    <td>YES</td>
    <td>NO</td>
  </tr>
  <tr>
    <td>Opera</td>
    <td>YES</td>
    <td>YES</td>
    <td>YES</td>
  </tr>
</table>
<code>*</code>From Edge 79
<h1>Media Types</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>File Format</th>
    <th>Media Type</th>
  </tr>
  <tr>
    <td>MP3</td>
    <td>audio/mpeg</td>
  </tr>
  <tr>
    <td>OGG</td>
    <td>audio/ogg</td>
  </tr>
  <tr>
    <td>WAV</td>
    <td>audio/wav</td>
  </tr>
</table>
<h1>Methods, Properties, and Events</h1>
The HTML DOM defines methods, properties, and events for the <b>&lt;audio&gt;</b> element.
<br>
This allows you to load, play, and pause audios, as well as set duration and volume.
<br>
There are also DOM events that can notify you when an audio begins to play, is paused, etc.
<table class="ws-table-all notranslate">
  <tr>
    <th>Tag</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>&lt;audio&gt;</td>
    <td>Defines sound content</td>
  </tr>
  <tr>
    <td>&lt;source&gt;</td>
    <td>Defines multiple media resources for media elements, such as &lt;video&gt; and &lt;audio&gt;</td>
  </tr>
</table>
