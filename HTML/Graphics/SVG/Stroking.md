<a href="/HTML/Graphics/SVG/Text.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Graphics/SVG/Filters/Main.md">Next &gt;</a>
<hr>
SVG offers a wide range of stroke properties. In this chapter we will look at the following:
<ul>
  <li>stroke</li>
  <li>stroke-width</li>
  <li>stroke-linecap</li>
  <li>stroke-dasharray</li>
</ul>
All the stroke properties can be applied to any kind of lines, text and outlines of elements like a circle.
<h1>stroke</h1>
<img src="https://i.imgur.com/YXbEvTQ.png">
<pre>&lt;svg height="80" width="300"&gt;&lt;g fill="none"&gt;&lt;path stroke="red" d="M5 20 l215 0" /&gt;&lt;path stroke="black" d="M5 40 l215 0" /&gt;&lt;path stroke="blue" d="M5 60 l215 0" /&gt;&lt;/g&gt;&lt;/svg&gt;</pre>
<h1>stroke-width</h1>
<img src="https://i.imgur.com/Ilk7LcM.png">
<pre>&lt;svg height="80" width="300"&gt;&lt;g fill="none" stroke="black"&gt;&lt;path stroke-width="2" d="M5 20 l215 0" /&gt;&lt;path stroke-width="4" d="M5 40 l215 0" /&gt;&lt;path stroke-width="6" d="M5 60 l215 0" /&gt;&lt;/g&gt;&lt;/svg&gt;</pre>
<h1>stroke-linecap</h1>
<img src="https://i.imgur.com/sWHNCG9.png">
<pre>&lt;svg height="80" width="300"&gt;&lt;g fill="none" stroke="black" stroke-width="6"&gt;&lt;path stroke-linecap="butt" d="M5 20 l215 0" /&gt;&lt;path stroke-linecap="round" d="M5 40 l215 0" /&gt;&lt;path stroke-linecap="square" d="M5 60 l215 0" /&gt;&lt;/g&gt;&lt;/svg&gt;</pre>
<h1>stroke-dasharray</h1>
<img src="https://i.imgur.com/iix7IWL.png">
<pre>&lt;svg height="80" width="300"&gt;&lt;g fill="none" stroke="black" stroke-width="4"&gt;&lt;path stroke-dasharray="5,5" d="M5 20 l215 0" /&gt;&lt;path stroke-dasharray="10,10" d="M5 40 l215 0" /&gt;&lt;path stroke-dasharray="20,10,5,5,5,10" d="M5 60 l215 0" /&gt;&lt;/g&gt;&lt;/svg&gt;</pre>
