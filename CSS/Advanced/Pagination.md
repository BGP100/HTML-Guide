Learn how to create a responsive pagination using CSS.
<h1>Simple</h1>
If you have a website with lots of pages, you may wish to add some sort of pagination to each page:
<br>
<img src="https://i.imgur.com/XoAAw3o.png">
<pre>
.pagination {
  display: inline-block;
}
.pagination a {
  color: black;
  float: left;
  padding: 8px 16px;
  text-decoration: none;
}
</pre>
<h1>Active</h1>
<img src="https://i.imgur.com/qVrPXQ0.png">
<pre>
.pagination a.active {
  background-color: #4CAF50;
  color: white;
}
</pre>
<h1>Borders</h1>
<img src="https://i.imgur.com/UPLHw41.png">
<br>
Use the <b>border</b> property to add borders to the pagination:
<pre>
.pagination a {
  border: 1px solid #ddd; /* Gray */
}
</pre>
<h1>Centered</h1>
<img src="https://i.imgur.com/3wEZOYq.png">
<br>
Change the size of the pagination with the <b>font-size</b> property:
<pre>
.pagination a {
  font-size: 22px;
}
</pre>
<h1>Breadcrums</h1>
<pre><a href="#Breadcrums">Home</a> / <a href="#Breadcrums">Pictures</a> / <a href="#Breadcrums">Summer 15</a> / <b>Italy</b></pre>
Another variation of pagination is so-called "breadcrumbs":
<pre>
ul.breadcrumb {
  padding: 8px 16px;
  list-style: none;
  background-color: #eee;
}
ul.breadcrumb li{display:inline;}
ul.breadcrumb li+li:before {
  padding: 8px;
  color: black;
  content: "/\00a0";
}
</pre>
