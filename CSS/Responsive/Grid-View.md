<h1>What is it?</h1>
Many web pages are based on a grid-view, which means that the page is divided into columns:
<br>
<img src="https://i.imgur.com/tW5H550.png" width="100%">
<br>
Using a grid-view is very helpful when designing web pages. It makes it easier to place elements on the page.
<br>
<img src="https://i.imgur.com/RU80Nng.png" width="100%">
<br>
A responsive grid-view often has 12 columns, and has a total width of 100%, and will shrink and expand as you resize the browser window.
<h1>Building it</h1>
Lets start building a responsive grid-view.
<br>
First ensure that all HTML elements have the box-sizing property set to border-box. This makes sure that the padding and border are included in the total width and height of the elements.
<br>
Add the following code in your CSS:
<pre>
* {
  box-sizing: border-box;
}
</pre>
Read more about the box-sizing property in our CSS Box Sizing chapter.
<br>
The following example shows a simple responsive web page, with two columns:
<br>
<img src="https://i.imgur.com/bKPU8zG.png" width="100%">
<pre>
.menu {
  width: 25%;
  float: left;
}
.main {
  width: 75%;
  float: left;
}
</pre>
The example above is fine if the web page only contains two columns.
<br>
However, we want to use a responsive grid-view with 12 columns, to have more control over the web page.
<br>
First we must calculate the percentage for one column: 100% / 12 columns = 8.33%.
<br>
Then we make one class for each of the 12 columns, <b>class="col-"</b> and a number defining how many columns the section should span:
<pre>
.col-1{width:8.33%;}
.col-2{width:16.66%;}
.col-3{width:25%;}
.col-4{width:33.33%;}
.col-5{width:41.66%;}
.col-6{width:50%;}
.col-7{width:58.33%;}
.col-8{width:66.66%;}
.col-9{width:75%;}
.col-10{width:83.33%;}
.col-11{width:91.66%;}
.col-12{width:100%;}
</pre>
All these columns should be floating to the left, and have a padding of 15px:
<pre>
[class*="col-"] {
  float: left;
  padding: 15px;
  border: 1px solid red;
}
</pre>
Each row should be wrapped in a <b>&lt;div&gt;</b>. The number of columns inside a row should always add up to 12:
<pre>
&lt;div class="row"&gt;
  &lt;div class="col-3"&gt;...&lt;/div&gt; &lt;!-- 25% --&gt;
  &lt;div class="col-9"&gt;...&lt;/div&gt; &lt;!-- 75% --&gt;
&lt;/div&gt;
</pre>
The columns inside a row are all floating to the left, and are therefore taken out of the flow of the page, and other elements will be placed as if the columns do not exist. To prevent this, we will add a style that clears the flow:
<pre>
.row::after {
  content: "";
  clear: both;
  display: table;
}
</pre>
We also want to add some styles and colors to make it look better:
<pre>
html {
  font-family: "Lucida Sans", sans-serif;
}
.header {
  background-color: #9933cc;
  color: #ffffff;
  padding: 15px;
}
.menu ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
.menu li {
  padding: 8px;
  margin-bottom: 7px;
  background-color :#33b5e5;
  color: #ffffff;
  box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
}
.menu li:hover {
  background-color: #0099cc;
}
</pre>
