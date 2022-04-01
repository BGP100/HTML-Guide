Learn how to style buttons using CSS.
<h1>Basic</h1>
<pre>
.button {
  background-color: #4CAF50; /* Green */
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
}
</pre>
<h1>Colors</h1>
<img src="https://i.imgur.com/9qvCjCW.png">
<img src="https://i.imgur.com/HLTe5Ae.png">
<img src="https://i.imgur.com/kRqjUyZ.png">
<img src="https://i.imgur.com/3JvXzan.png">
<img src="https://i.imgur.com/3dJzFVt.png">
<br>
Use the <b>background-color</b> property to change the background color of a button:
<pre>
button.test1{background-color:#4CAF50;} /* Green */
button.test2{background-color:#008CBA;} /* Blue */
button.test3{background-color:#f44336;} /* Red */
button.test4{background-color:#e7e7e7;color:black;} /* Gray */
button.test5{background-color:#555555;} /* Black */
</pre>
<h1>Sizes</h1>
<img src="https://i.imgur.com/jZIsNGM.png">
<img src="https://i.imgur.com/4UxZs5V.png">
<img src="https://i.imgur.com/Kt2eHb0.png">
<img src="https://i.imgur.com/T7vaFYP.png">
<img src="https://i.imgur.com/Sz0M8SB.png">
<br>
Use the font-size property to change the font size of a button:
<pre>
button.test{font-size:10px;}
button.test{font-size:12px;}
button.test{font-size:16px;}
button.test{font-size:20px;}
button.test{font-size:24px;}
</pre>
<h1>Rounded</h1>
<img src="https://i.imgur.com/o4r62lP.png">
<img src="https://i.imgur.com/44VITl2.png">
<img src="https://i.imgur.com/B3SG3E1.png">
<img src="https://i.imgur.com/bZexhdq.png">
<img src="https://i.imgur.com/fM81Yeg.png">
<br>
Use the <b>border-radius</b> property to add rounded corners to a button:
<pre>
button.test1{border-radius:2px;}
button.test2{border-radius:4px;}
button.test3{border-radius:8px;}
button.test4{border-radius:12px;}
button.test5{border-radius:50%;}
</pre>
<h1>Shadow</h1>
Use the <b>box-shadow</b> property to add shadows to a button:
<pre>
button.test1 {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
}
button.test2:hover {
  box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24), 0 17px 50px 0 rgba(0,0,0,0.19);
}
</pre>
<h1>Width</h1>
<img src="https://i.imgur.com/od9qsb3.png" width="25%">
<br>
<img src="https://i.imgur.com/y2awTvT.png" width="50%">
<img src="https://i.imgur.com/qxGvFji.png" width="100%">
<br>
By default, the size of the button is determined by its text content (as wide as its content). Use the width property to change the width of a button:
<pre>
button.test1{width:250px;}
button.test2{width:50%;}
button.test3{width:100%;}
</pre>
<h1>Button on Image</h1>
<img src="https://i.imgur.com/TexuWPt.png">
