<a href="/CSS/Dropdown.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/ImageSprites.md">Next &gt;</a>
<hr>
CSS can be used to create an image gallery.
<br>
<img src="https://i.imgur.com/pm8imha.png">
<img src="https://i.imgur.com/SvodqWN.png">
<img src="https://i.imgur.com/ZxE0ZjY.png">
<img src="https://i.imgur.com/Sq1tP3B.png">
<hr>
The following image gallery is created with CSS:
<pre>
&lt;style&gt;
div.gallery {
  margin: 5px;
  border: 1px solid #ccc;
  float: left;
  width: 180px;
}
div.gallery:hover {
  border: 1px solid #777;
}
div.gallery img {
  width: 100%;
  height: auto;
}
div.desc {
  padding: 15px;
  text-align: center;
}
&lt;/style&gt;
&lt;div class="gallery"&gt;
  &lt;a target="_blank" href="img_5terre.jpg"&gt;
    &lt;img src="img_5terre.jpg" alt="Cinque Terre" width="600" height="400"&gt;
  &lt;/a&gt;
  &lt;div class="desc"&gt;Add a description of the image here&lt;/div&gt;
&lt;/div&gt;
&lt;div class="gallery"&gt;
  &lt;a target="_blank" href="img_5terre.jpg"&gt;
    &lt;img src="img_forest.jpg" alt="Cinque Terre" width="600" height="400"&gt;
  &lt;/a&gt;
  &lt;div class="desc"&gt;Add a description of the image here&lt;/div&gt;
&lt;/div&gt;
&lt;div class="gallery"&gt;
  &lt;a target="_blank" href="img_5terre.jpg"&gt;
    &lt;img src="img_lights.jpg" alt="Cinque Terre" width="600" height="400"&gt;
  &lt;/a&gt;
  &lt;div class="desc"&gt;Add a description of the image here&lt;/div&gt;
&lt;/div&gt;
&lt;div class="gallery"&gt;
  &lt;a target="_blank" href="img_5terre.jpg"&gt;
    &lt;img src="img_mountains.jpg" alt="Cinque Terre" width="600" height="400"&gt;
  &lt;/a&gt;
  &lt;div class="desc"&gt;Add a description of the image here&lt;/div&gt;
&lt;/div&gt;
</pre>
<h1>Example</h1>
<img src="https://i.imgur.com/VhXk4X3.jpg">
