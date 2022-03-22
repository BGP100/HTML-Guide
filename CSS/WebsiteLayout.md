A website is often divided into headers, menus, content and a footer:
<br>
<img src="https://i.imgur.com/cNZ3KpI.jpg" width="80%">
<br>
There are tons of different layout designs to choose from. However, the structure above, is one of the most common, and we will take a closer look at it in this tutorial.
<h1>Header</h1>
A header is usually located at the top of the website (or right below a top navigation menu). It often contains a logo or the website name:
<pre>
.header {
  background-color: #F1F1F1;
  text-align: center;
  padding: 20px;
}
</pre>
<img src="https://i.imgur.com/FJ7VTcA.jpg" width="80%">
<h1>Navigation Bar</h1>
<b>Tip:</b> go to my <a href="CSS/NavigationBar/">Navigation Bar Chapters</a> for more info.
<br>
A navigation bar contains a list of links to help visitors navigating through your website:
<pre>
/* The navbar container */
.topnav {
  overflow: hidden;
  background-color: #333;
}
/* Navbar links */
.topnav a {
  float: left;
  display: block;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}
/* Links - change color on hover */
.topnav a:hover {
  background-color: #ddd;
  color: black;
}
</pre>
<img src="https://i.imgur.com/iX1km0H.jpg" width="80%">
<h1>Content</h1>
The layout in this section, often depends on the target users. The most common layout is one (or combining them) of the following:
<ul>
  <li><b>1-column</b> (often used for mobile browsers)<li>
  <li><b>2-column</b> (often used for tablets and laptops)</li>
  <li><b>3-column</b> layout (only used for desktops)</li>
</ul>
<img src="https://i.imgur.com/YvRdxvy.jpg" width="25%"><img src="https://i.imgur.com/EMGwRVs.jpg" width="25%"><img src="https://i.imgur.com/V4nzsdH.jpg" width="25%">
<br>
We will create a 3-column layout, and change it to a 1-column layout on smaller screens:
<pre>
/* Create three equal columns that float next to each other */
.column {
  float: left;
  width: 33.33%;
}
/* Clear floats after the columns */
.row:after {
  content: "";
  display: table;
  clear: both;
}
/* Responsive layout - makes the three columns stack on top of each other instead of next to each other on smaller screens (600px wide or less) */
@media screen and (max-width: 600px) {
  .column {
    width: 100%;
  }
}
</pre>
<img src="https://i.imgur.com/WoiDfCE.jpg" width="80%">
<h1>Unequal Columns</h1>
The main content is the biggest and the most important part of your site.
<br>
It is common with <b>unequal</b> column widths, so that most of the space is reserved for the main content. The side content (if any) is often used as an alternative navigation or to specify information relevant to the main content. Change the widths as you like, only remember that it should add up to 100% in total:
<pre>
.column {
  float: left;
}
/* Left and right column */
.column.side {
  width: 25%;
}
/* Middle column */
.column.middle {
  width: 50%;
}
/* Responsive layout - makes the three columns stack on top of each other instead of next to each other */
@media screen and (max-width: 600px) {
  .column.side, .column.middle {
    width: 100%;
  }
}
</pre>
<img src="https://i.imgur.com/10n36M3.jpg" width="80%">
<h1>Footer</h1>
The footer is placed at the bottom of your page. It often contains information like copyright and contact info:
<pre>
.footer {
  background-color: #F1F1F1;
  text-align: center;
  padding: 10px;
}
</pre>
<img src="https://i.imgur.com/LNOoJCW.jpg" width="80%">
