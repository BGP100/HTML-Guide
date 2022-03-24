The <b>&lt;applet&gt;</b> tag was used in HTML 4 to define an embedded applet (Plug-in).
<br>
By this, I mean that this tag is not supported in the current version.
<h1>Plug-ins</h1>
Plug-ins are a computer programs that extend the standard functionality of the browser.
<br>
Plug-ins have been used for many different purposes:
<ul>
  <li>Run Java applets</li>
  <li>Run ActiveX controls</li>
  <li>Display Flash movies</li>
  <li>Display maps</li>
  <li>Scan for viruses</li>
  <li>Verify a bank id</li>
</ul>
<h1>What to do?</h1>
If you want to embed a video, use the <b>&lt;video&gt;</b> tag:
<pre>
&lt;video width="320" height="240" controls&gt;
  &lt;source src="movie.mp4" type="video/mp4"&gt;
  &lt;source src="movie.ogg" type="video/ogg"&gt;
  Your browser does not support the video tag.
&lt;/video&gt;
</pre>
