Before you continue you should have a basic understanding of the following:
<ul>
  <li><a href="/HTML/">HTML</a></li>
  <li><a href="/CSS/">CSS</a></li>
</ul>
<h1>What is it?</h1>
<ul>
  <li>Sass stands for <strong>S</strong>yntactically <strong>A</strong>wesome <strong>S</strong>tyle<strong>S</strong>heets.</li>
  <li>Sass is an extension to CSS.</li>
  <li>Sass is a CSS pre-processor.</li>
  <li>Sass is completely compatible with all versions of CSS.</li>
  <li>Sass reduces repetition of CSS and therefore saves time.</li>
  <li>Sass was designed by Hampton Catlin and developed by Natalie Weizenbaum in 2006.</li>
  <li>Sass is free to download and use.</li>
</ul>
<h1>A Simple Example why Sass is Useful</h1>
Let's say we have a website with three main colors:
<br>
<img src="https://i.imgur.com/RPZeSMi.png">
<br>
So, how many times do you need to type those HEX values? A LOT of times. And what about variations of the same colors?
<br>
Instead of typing the above values a lot of times, you can use Sass and write this:
<pre>
/* define variables for the primary colors */
$color-1: #a2b9bc;
$color-2: #b2ad7f;
$color-3: #878f99;
/* use the variables */
.main-header {
  background-color: $color-1;
}
.menu-left {
  background-color: $color-2;
}
.menu-right {
  background-color: $color-3;
}
</pre>
So, when using Sass, and the primary color changes, you only need to change it in one place.
<h1>How Does it Work?</h1>
A browser does not understand Sass code. Therefore, you will need a Sass pre-processor to convert Sass code into standard CSS.
<br>
This process is called transpiling. So, you need to give a transpiler (some kind of program) some Sass code and then get some CSS code back.
<h1>File Extension</h1>
Sass files has the ".scss" file extension.
<h1>Comments</h1>
Sass supports standard CSS comments <code>/* comment */</code>, and in addition it supports inline comments <code>// comment</code>:
<pre>/* Hello this is a comment */</pre>
<pre>// Hello this is a comment //</pre>
