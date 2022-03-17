This page contains common float examples.
<hr>
<img src="https://i.imgur.com/qIn59vB.jpg" width="69%">
<br>
<img src="https://i.imgur.com/rXQPqqG.jpg" width="69%">
<pre>
* {
  box-sizing: border-box;
}
.box {
  float: left;
  width: 33.33%; /* three boxes (use 25% for four, and 50% for two, etc) */
  padding: 50px; /* if you want space between the images */
}
</pre>
<hr>
<img src="https://i.imgur.com/ZWmO5em.jpg" width="69%">
<pre>
.box {
  height: 500px;
}
</pre>
<img src="https://i.imgur.com/EE7hPhs.jpg" width="69%">
<pre>
.box {
  background-color: #f1f1f1;
  width: 50%;
  margin: 10px;
  text-align: center;
  line-height: 75px;
  font-size: 30px;
}
</pre>
<hr>
<img src="https://i.imgur.com/DZEPiFQ.jpg" width="69%">
<pre>
ul {
  list-style-type: none;
  margin: 0;
  padding; 0;
  overflow: hidden;
  background-color: #333;
}
li {
  float: left;
}
li a {
  display: inline-block;
  color: white;
  text-aligh: center;
  padding: 14px 16px;
  text-decoration: none;
}
li a:hover {
  background-color: #111;
}
.active {
  background-color: red;
}
</pre>
<hr>
<img src="https://i.imgur.com/ehpPv3J.jpg" width="69%">
<pre>
.header, .footer {
  background-color: grey;
  color: white;
  padding: 15px;
}
.column {
  float: left;
  padding: 15px;
}
.clearfix::after {
  content: "";
  clear: both;
  display: table;
}
.menu {
  width: 25%;
}
.content {
  width: 75%;
}
</pre>
