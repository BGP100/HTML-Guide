<a href="/JS/BOM/Window.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/BOM/Location.md">Next &gt;</a>
<hr>
The <b>window.screen</b> object contains information about the user's screen.
<h1>Window Screen</h1>
The <b>window.screen</b> object can be written without the window prefix.
<br>
Properties:
<ul>
  <li><b>screen.width</b></li>
  <li><b>screen.height</b></li>
  <li><b>screen.availWidth</b></li>
  <li><b>screen.availHeight</b></li>
  <li><b>screen.colorDepth</b></li>
  <li><b>screen.pixelDepth</b></li>
</ul>
<h1>Width</h1>
The <b>screen.width</b> property returns the width of the visitor's screen in pixels.
<pre>document.getElementById("demo").innerHTML = "Screen Width: " + screen.width;</pre>
<h1>Height</h1>
The <b>screen.height</b> property returns the height of the visitor's screen in pixels.
<pre>document.getElementById("demo").innerHTML = "Screen Height: " + screen.height;</pre>
<h1>Available Width</h1>
The <b>screen.availWidth</b> property returns the width of the visitor's screen, in pixels, minus interface features like the Windows Taskbar.
<pre>document.getElementById("demo").innerHTML = "Available Screen Width: " + screen.availWidth;</pre>
<h1>Available Height</h1>
The <b>screen.availHeight</b> property returns the height of the visitor's screen, in pixels, minus interface features like the Windows Taskbar.
<pre>document.getElementById("demo").innerHTML = "Available Screen Height: " + screen.availHeight;</pre>
<h1>Color Depth</h1>
The <b>screen.colorDepth</b> property returns the number of bits used to display one color.
<br>
All modern computers use 24 bit or 32 bit hardware for color resolution:
<ul>
  <li>24 bits = 16,777,216 different "True Colors"</li>
  <li>32 bits = 4,294,967,296 different "Deep Colors"</li>
</ul>
Older computers used 16 bits: 65,536 different "High Colors" resolution.
<br>
Very old computers, and old cell phones used 8 bits: 256 different "VGA colors".
<pre>document.getElementById("demo").innerHTML = "Screen Color Depth: " + screen.colorDepth;</pre>
<h1>Pixel Depth</h1>
The <b>screen.pixelDepth</b> property returns the pixel depth of the screen.
<pre>document.getElementById("demo").innerHTML = "Screen Pixel Depth: " + screen.pixelDepth;</pre>
