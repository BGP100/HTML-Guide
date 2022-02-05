With HTML image maps, you can create clickable areas on an image.
<br>
The HTML <b>&lt;map&gt;</b> tag defines an image map. An image map is an image with clickable areas. The areas are defined with one or more <b>&lt;area&gt;</b> tags.
<br>
Try to click on the computer, phone, or the cup of coffee in the image below:
<br>
<img src="https://www.w3schools.com/html/workplace.jpg">
<pre>
&lt;img src="//www.w3schools.com/html/workplace.jpg" alt="Workplace" usemap="#workmap"&gt;
&lt;map name="workmap"&gt;
  &lt;area shape="rect" coords="34,44,270,350" alt="Computer" href="computer.htm"&gt;
  &lt;area shape="rect" coords="290,172,333,250" alt="Phone" href="phone.htm"&gt;
  &lt;area shape="circle" coords="337,300,44" alt="Coffee" href="coffee.htm"&gt;
&lt;/map&gt;
</pre>
<h1>How does it work?</h1>
The idea behind an image map is that you should be able to perform different actions depending on where in the image you click.
<br>
To create an image map you need an image, and some HTML code that describes the clickable areas.
<h1>Create Map</h1>
Add a <b>&lt;map&gt;</b> element.
<br>
The <b>&lt;map&gt;</b> element is used to create an image map, and is linked to the image by using the required name attribute:
<pre>&lt;map name="workmap"&gt;</pre>
The name attribute must have the same value as the <b>&lt;map&gt;</b>'s usemap attribute.
<h1>Areas</h1>
Then, add the clickable areas.
<br>
A clickable area is defined using an <area> element.
<br>
You must define the shape of the clickable area, and you can choose one of these values:
<ul>
  <li>rect - defines a rectangular region.</li>
  <li>circle - defines a circular region.</li>
  <li>poly - defines a polygonal region.</li>
  <li>default - defines the entire region.</li>
</ul>
You must also define some coordinates to be able to place the clickable area onto the image.
<h1>shape="rect"</h1>
The coordinates for shape="rect" come in pairs, one for the x-axis and one for the y-axis.
<br>
So, the coordinates 34,44 is located 34 pixels from the left margin and 44 pixels from the top:
<img src="https://images.alalgi.repl.co/638.png" alt="Workplace">
The coordinates 270,350 is located 270 pixels from the left margin and 350 pixels from the top:
<img src="https://images.alalgi.repl.co/193.png" alt="Workplace">
Now we have enough data to create a clickable rectangular area:
<pre>&lt;area shape="rect" coords="34,44,270,350" href="computer.htm"&gt;</pre>
This is the area that becomes clickable and will send the user to the page "computer.htm":
<img src="https://images.alalgi.repl.co/837.png" alt="Workplace">
<h1>shape="circle"</h1>
To add a circle area, first locate the coordinates of the center of the circle: 337,300
<img src="https://images.alalgi.repl.co/743.png" alt="Workplace">
Then specify the radius of the circle: 44 pixels
<img src="https://images.alalgi.repl.co/285.png" alt="Workplace">
Now you have enough data to create a clickable circular area:
<pre>&lt;area shape="circle" coords="337, 300, 44" href="coffee.htm"&gt;</pre>
This is the area that becomes clickable and will send the user to the page "coffee.htm":
<img src="https://images.alalgi.repl.co/547.png" alt="Workplace">
<h1>shape="poly"</h1>
The <b>shape="poly"</b> contains several coordinate points, which creates a shape formed with straight lines (a polygon).
<br>
This can be used to create any shape.
<br>
Like maybe a croissant shape!
<br>
How can we make the croissant in the image below become a clickable link?
<img src="https://www.w3schools.com/html/frenchfood.jpg">
We have to find the x and y coordinates for all edges of the croissant:
<img src="https://www.w3schools.com/html/frenchfood4.jpg">
The coordinates come in pairs, one for the x-axis and one for the y-axis:
<pre>&lt;area shape="poly" coords="140,121,181,116,204,160,204,222,191,270,140,329,85,355,58,352,37,322,40,259,103,161,128,147" href="croissant.htm"&gt;</pre>
This is the area that becomes clickable and will send the user to the page "croissant.htm":
<img src="https://www.w3schools.com/html/frenchfood3.jpg">
<h1>Map with JavaScript</h1>
A clickable area can also trigger a JavaScript function.
<br>
Add a click event to the <b>&lt;area&gt;</b> element to execute a JavaScript function:
<pre>
&lt;map name="workmap"&gt;
  &lt;area shape="circle" coords="337,300,44" href="coffee.htm" onclick="myFunction()"&gt;
&lt;/map&gt;
&lt;script&gt;
function myFunction() {
  alert("You clicked the coffee cup!");
}
&lt;/script&gt;
</pre>
<h1>Tags</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>Tag</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><a href="/tags/tag_img.asp">&lt;img&gt;</a></td>
    <td>Defines an image</td>
  </tr>
  <tr>
    <td><a href="/tags/tag_map.asp">&lt;map&gt;</a></td>
    <td>Defines an image map</td>
  </tr>
  <tr>
    <td><a href="/tags/tag_area.asp">&lt;area&gt;</a></td>
    <td>Defines a clickable area inside an image map</td>
  </tr>
  <tr>
    <td><a href="/tags/tag_picture.asp">&lt;picture&gt;</a></td>
    <td>Defines a container for multiple image resources</td>
  </tr>
</table>
