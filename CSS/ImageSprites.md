<a href="/CSS/ImageGallery.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/AttributeSelectors.md">Next &gt;</a>
<hr>
An image sprite is a collection of images put into a single image.
<br>
A web page with many images can take a long time to load and generates multiple server requests.
<br>
Using image sprites will reduce the number of server requests and save bandwidth.
<h1>Simple Example</h1>
Instead of using three separate images, we use this single image ("//i.imgur.com/ntYd1yD.gif"):
<br>
<img src="https://i.imgur.com/ntYd1yD.gif">
<br>
With CSS, we can show just the part of the image we need.
<br>
In the following example the CSS specifies which part of the "//i.imgur.com/ntYd1yD.gif" image to show:
<pre>
#home {
  width: 46px;
  height: 44px;
  background: url(//i.imgur.com/ntYd1yD.gif) 0 0;
}
</pre>
<b>Explained:</b>
<ul>
  <li><b>&lt;img id="home" src="img_trans.gif"&gt;</b> - Only defines a small transparent image because the src attribute cannot be empty. The displayed image will be the background image we specify in CSS</li>
  <li><b>width: 46px; height: 44px;</b> - Defines the portion of the image we want to use</li>
  <li><b>background: url(img_navsprites.gif) 0 0;</b> - Defines the background image and its position (left 0px, top 0px)</li>
</ul>
This is the easiest way to use image sprites, now we want to expand it by using links and hover effects.
<h1>Navigation List</h1>
We want to use the sprite image ("//i.imgur.com/ntYd1yD.gif") to create a navigation list.
<br>
We will use an HTML list, because it can be a link and also supports a background image:
<pre>
#navlist {
  position: relative;
}
#navlist li {
  margin: 0;
  padding: 0;
  list-style: none;
  position: absolute;
  top: 0;
}
#navlist li, #navlist a {
  height: 44px;
  display: block;
}
#home {
  left: 0px;
  width: 46px;
  background: url('img_navsprites.gif') 0 0;
}
#prev {
  left: 63px;
  width: 43px;
  background: url('img_navsprites.gif') -47px 0;
}
#next {
  left: 129px;
  width: 43px;
  background: url('img_navsprites.gif') -91px 0;
}
</pre>
<b>Explained:</b>
<ul>
  <li>#navlist {position:relative;} - position is set to relative to allow absolute positioning inside it</li>
  <li>#navlist li {margin:0;padding:0;list-style:none;position:absolute;top:0;} - margin and padding are set to 0, list-style is removed, and all list items are absolute positioned</li>
  <li>#navlist li, #navlist a {height:44px;display:block;} - the height of all the images are 44px</li>
</ul>
Now start to position and style for each specific part:
<ul>
  <li>#home {left:0px;width:46px;} - Positioned all the way to the left, and the width of the image is 46px</li>
  <li>#home {background:url(img_navsprites.gif) 0 0;} - Defines the background image and its position (left 0px, top 0px)</li>
  <li>#prev {left:63px;width:43px;} - Positioned 63px to the right (#home width 46px + some extra space between items), and the width is 43px.</li>
  <li>#prev {background:url('img_navsprites.gif') -47px 0;} - Defines the background image 47px to the right (#home width 46px + 1px line divider)</li>
  <li>#next {left:129px;width:43px;}- Positioned 129px to the right (start of #prev is 63px + #prev width 43px + extra space), and the width is 43px.</li>
  <li>#next {background:url('img_navsprites.gif') -91px 0;} - Defines the background image 91px to the right (#home width 46px + 1px line divider + #prev width 43px + 1px line divider)</li>
</ul>
<h1>Hover</h1>
Now we want to add a hover effect to our navigation list.
<br>
<b><i>Tip:</i></b> The <b>:hover</b> selector can be used on all elements, not only on links.
<br>
Our new image ("img_navsprites_hover.gif") contains three navigation images and three images to use for hover effects:
<br>
<img src="https://i.imgur.com/mHwn5iU.gif">
<br>
Because this is one single image, and not six separate files, there will be no loading delay when a user hovers over the image.
<br>
We only add three lines of code to add the hover effect:
<pre>
#home a:hover {
  background: url('img_navsprites_hover.gif') 0 -45px;
}
#prev a:hover {
  background: url('img_navsprites_hover.gif') -47px -45px;
}
#next a:hover {
  background: url('img_navsprites_hover.gif') -91px -45px;
}
</pre>
<b>Explained:</b>
<ul>
#home a:hover {background: url('img_navsprites_hover.gif') 0 -45px;} - For all three hover images we specify the same background position, only 45px further down
</ul>
