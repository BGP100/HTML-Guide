<a href="/CSS/Advanced/Home.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Advanced/BorderImages.md">Next &gt;</a>
<hr>
With the CSS <b>border-radius</b> property, you can give any element "rounded corners".
<hr>
The CSS border-radius property defines the radius of an element's corners.
<br>
<b>Tip:</b> This property allows you to add rounded corners to elements!
<br>
Here are three examples:
<br>
1. Rounded corners for an element with a specified background color:
<br>
<img src="https://i.imgur.com/2P80aqI.jpg" width="23%">
<br>
2. Rounded corners for an element with a border:
<br>
<img src="https://i.imgur.com/DBCNYaI.jpg" width="23%">
<br>
3. Rounded corners for an element with a background image:
<br>
<img src="https://i.imgur.com/UcrFVV8.jpg" width="23%">
<br>
Here is the code:
<pre>
#rcorners1 {
  border-radius: 25px;
  background: #73AD21;
  padding: 20px; 
  width: 200px;
  height: 150px; 
}
#rcorners2 {
  border-radius: 25px;
  border: 2px solid #73AD21;
  padding: 20px; 
  width: 200px;
  height: 150px; 
}
#rcorners3 {
  border-radius: 25px;
  background: url(//i.imgur.com/RaRoUUk.gif);
  background-position: left top;
  background-repeat: repeat;
  padding: 20px; 
  width: 200px;
  height: 150px; 
}
</pre>
<h1>Specify Each Corner</h1>
The border-radius property can have from one to four values. Here are the rules:
<br>
<b>Four values - border-radius: 15px 50px 30px 5px;</b> (first value applies to top-left corner, second value applies to top-right corner, third value applies to bottom-right corner, and fourth value applies to bottom-left corner):
<br>
<img src="https://i.imgur.com/7NBpTt4.jpg" width="23%">
<br>
<b>Three values - border-radius: 15px 50px 30px;</b> (first value applies to top-left corner, second value applies to top-right and bottom-left corners, and third value applies to bottom-right corner):
<br>
<img src="https://i.imgur.com/nWm3rop.jpg" width="23%">
<br>
<b>Two values - border-radius: 15px 50px;</b> (first value applies to top-left and bottom-right corners, and the second value applies to top-right and bottom-left corners):
<br>
<img src="https://i.imgur.com/mBI9NAe.jpg" width="23%">
<br>
<b>One value - border-radius: 15px;</b> (the value applies to all four corners, which are rounded equally:
<br>
<img src="https://i.imgur.com/YNCwODm.jpg" width="23%">
<pre>
#rcorners1 {
  border-radius: 15px 50px 30px 5px;
  background: #73AD21;
  padding: 20px; 
  width: 200px;
  height: 150px; 
}
#rcorners2 {
  border-radius: 15px 50px 30px;
  background: #73AD21;
  padding: 20px; 
  width: 200px;
  height: 150px; 
}
#rcorners3 {
  border-radius: 15px 50px;
  background: #73AD21;
  padding: 20px; 
  width: 200px;
  height: 150px; 
}
#rcorners4 {
  border-radius: 15px;
  background: #73AD21;
  padding: 20px; 
  width: 200px;
  height: 150px; 
}
</pre>
You could also create elliptical corners:
<pre>
#rcorners1 {
  border-radius: 50px / 15px;
  background: #73AD21;
  padding: 20px; 
  width: 200px;
  height: 150px; 
}
#rcorners2 {
  border-radius: 15px / 50px;
  background: #73AD21;
  padding: 20px; 
  width: 200px;
  height: 150px; 
}
#rcorners3 {
  border-radius: 50%;
  background: #73AD21;
  padding: 20px; 
  width: 200px;
  height: 150px;
}
</pre>
