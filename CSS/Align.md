<img src="https://i.imgur.com/IHOSJBM.jpg" width="100%">
<h1>Center Elements</h1>
To horizontally center a block element (like <b>&lt;div&gt;</b>), use <b>margin: auto;</b>
<br>
Setting the width of the element will prevent it from stretching out to the edges of its container.
<br>
The element will then take up the specified width, and the remaining space will be split equally between the two margins:
<br>
<img src="https://i.imgur.com/LDrvE9p.jpg" width="100%">
<pre>
.center {
  margin: auto;
  width: 50%;
  border: 3px solid green;
  padding: 10px;
}
</pre>
<h1>Center Text</h1>
To just center the text inside an element, use <b>text-align: center;</b>
<br>
<img src="https://i.imgur.com/Y7lwMEz.jpg" width="100%">
<pre>
.center {
  text-align: center;
  border: 3px solid green;
}
</pre>
<h1>Center Images</h1>
To center an image, set left and right margin to <b>auto</b> and make it into a <b>block</b> element:
<br>
<img src="https://i.imgur.com/bbdrlJP.jpg" width="100%">
<pre>
img {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 40%;
}
</pre>
<h1>Left &amp; Right</h1>
<h2>Position</h2>
One method for aligning elements is to use <b>position: absolute;</b>:
<br>
<img src="https://i.imgur.com/cGMKq0T.jpg" width="100%">
<pre>
.right {
  position: absolute;
  right: 0px;
  width: 300px;
  border: 3px solid #73AD21;
  padding: 10px;
}
</pre>
<h2>Float</h2>
Another method for aligning elements is to use the <b>float</b> property:
<pre>
.right {
  float: right;
  width: 300px;
  border: 3px solid #73AD21;
  padding: 10px;
}
</pre>
<h1>Clearfix</h1>
Then we can add the clearfix hack to the containing element to fix this problem:
<br>
<b>Without:</b>
<br>
<img src="https://i.imgur.com/rVDfETJ.jpg" width="50%">
<br>
<b>With:</b>
<br>
<img src="https://i.imgur.com/vuK09kv.jpg" width="50%">
<pre>
.clearfix::after {
  content: "";
  clear: both;
  display: table;
}
</pre>
<h1>Center Vertically</h1>
There are many ways to center an element vertically in CSS. A simple solution is to use top and bottom padding:
<br>
<img src="https://i.imgur.com/xaLoYDh.jpg" width="100%">
<pre>
.center {
  padding: 70px 0;
  border: 3px solid green;
}
</pre>
<h1>Center Vertically &amp; Horizontally</h1>
To center both vertically and horizontally, use padding and <b>text-align: center;</b>:
<br>
<img src="https://i.imgur.com/pVrgUYI.jpg" width="100%">
<pre>
.center {
  padding: 70px 0;
  border: 3px solid green;
  text-align: center;
}
</pre>
<h2>line-height</h2>
Another trick is to use the <b>line-height</b> property with a value that is equal to the <b>height</b> property:
<br>
<img src="https://i.imgur.com/pVrgUYI.jpg" width="100%">
<pre>
.center {
  line-height: 200px;
  height: 200px;
  border: 3px solid green;
  text-align: center;
}
/* If the text has multiple lines, add the following: */
.center p {
  line-height: 1.5;
  display: inline-block;
  vertical-align: middle;
}
</pre>
<h2>Position &amp; Transition</h2>
If <b>padding</b> and <b>line-height</b> are not options, another solution is to use positioning and the <b>transform</b> property:
<br>
<img src="https://i.imgur.com/pVrgUYI.jpg" width="100%">
<pre>
.center { 
  height: 200px;
  position: relative;
  border: 3px solid green; 
}
.center p {
  margin: 0;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</pre>
<h2>Flexbox</h2>
You can also use flexbox to center things. Just note that flexbox is not supported in IE10 and earlier versions:
<br>
<img src="https://i.imgur.com/pVrgUYI.jpg" width="100%">
<pre>
.center {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 200px;
  border: 3px solid green; 
}
</pre>
