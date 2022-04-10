<a href="/CSS/Advanced/Tooltip.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Advanced/ImageReflection.md">Next &gt;</a>
<hr>
<h1>Rounded</h1>
Use the border-radius property to create rounded images:
<br>
<img src="https://i.imgur.com/HGerZP9.png">
<pre>
img {
  border-radius: 8px;
}
</pre>
<img src="https://i.imgur.com/cFw1CQA.png">
<pre>
img {
  border-radius: 50%;
}
</pre>
<h1>Thumbnail</h1>
Use the <b>border</b> property to create thumbnail images.
<br>
<img src="https://i.imgur.com/fnb7Hiw.png">
<pre>
&lt;style&gt;
img {
  border: 1px solid #ddd;
  border-radius: 4px;
  padding: 5px;
  width: 150px;
}
&lt;/style&gt;
&lt;img src="paris.jpg" alt="Paris"&gt;
</pre>
<h1>Responsive</h1>
Responsive images will automatically adjust to fit the size of the screen.
<br>
Resize the browser window to see the effect:
<br>
<img src="https://i.imgur.com/JwssDZj.png" width="100%">
<br>
If you want an image to scale down if it has to, but never scale up to be larger than its original size, add the following:
<pre>
img {
  max-width: 100%;
  height: auto;
}
</pre>
<b>Tip:</b> Read more about Responsive Web Design in my <a href="Responsive/">CSS Responsive Tutorial</a>.
<h1>Center Imgs</h1>
To center an image, set left and right margin to auto and make it into a block element:
<br>
<img src="https://i.imgur.com/3twCBbT.png" width="100%">
<pre>
img {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 50%;
}
</pre>
<h1>Opacity</h1>
The <b>opacity</b> property can take a value from 0.0 - 1.0. The lower value, the more transparent:
<br>
<b>0.2 Opacity:</b>
<br>
<img src="https://i.imgur.com/Aw3IHWe.png" width="286px" height="190px">
<br>
<b>0.5 Opacity:</b>
<br>
<img src="https://i.imgur.com/Onh3HPn.png" width="286px" height="190px">
<br>
<b>1.0 Opacity (default):</b>
<br>
<img src="https://i.imgur.com/FPZIybF.png" width="286px" height="190px">
<pre>
img {
  opacity: 0.5;
}
</pre>
<h1>Image Modal (Advanced)</h1>
This is an example to demonstrate how CSS and JavaScript can work together.
<br>
First, use CSS to create a modal window (dialog box), and hide it by default.
<br>
Then, use a JavaScript to show the modal window and to display the image inside the modal, when a user clicks on the image:
<pre>
// Get the modal
var modal = document.getElementById('myModal');
// Get the image and insert it inside the modal - use its "alt" text as a caption
var img = document.getElementById('myImg');
var modalImg = document.getElementById("img01");
var captionText = document.getElementById("caption");
img.onclick = function(){
  modal.style.display = "block";
  modalImg.src = this.src;
  captionText.innerHTML = this.alt;
}
// Get the &lt;span&gt; element that closes the modal
var span = document.getElementsByClassName("close")[0];
// When the user clicks on &lt;span&gt; (x), close the modal
span.onclick = function() {
  modal.style.display = "none";
}
</pre>
