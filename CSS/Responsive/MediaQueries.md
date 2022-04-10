<a href="/CSS/Responsive/Grid-View.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Responsive/Images.md">Next &gt;</a>
<hr>
Media query is a CSS technique introduced in CSS3.
<br>
It uses the <b>@media</b> rule to include a block of CSS properties only if a certain condition is true.
<pre>
@media only screen and (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
</pre>
<h1>Breakpoints</h1>
Earlier in this tutorial we made a web page with rows and columns, and it was responsive, but it did not look good on a small screen.
<br>
Media queries can help with that. We can add a breakpoint where certain parts of the design will behave differently on each side of the breakpoint.
<p></p>
<b>Desktop:</b> <img src="https://i.imgur.com/lIRIeMw.png">
<br>
<b>Phone:</b> <img src="https://i.imgur.com/1Z1rgr1.png">
<br>
Use a media query to add a breakpoint at 768px:
<pre>
/* For desktop: */
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
@media only screen and (max-width: 768px) {
  /* For mobile phones: */
  [class*="col-"] {
    width: 100%;
  }
}
</pre>
<h1>Always Mobile Design First</h1>
Mobile First means designing for mobile before designing for desktop or any other device (This will make the page display faster on smaller devices).
<br>
This means that we must make some changes in our CSS.
<br>
Instead of changing styles when the width gets smaller than 768px, we should change the design when the width gets larger than 768px. This will make our design Mobile First:
<pre>
/* For mobile phones: */
[class*="col-"] {
  width: 100%;
}
@media only screen and (min-width: 768px) {
  /* For desktop: */
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
}
</pre>
<h1>Another Breakpoint</h1>
You can add as many breakpoints as you like.
<br>
We will also insert a breakpoint between tablets and mobile phones.
<p></p>
<b>Desktop:</b> <img src="https://i.imgur.com/lIRIeMw.png">
<br>
<b>Tablet:</b> <img src="https://i.imgur.com/RlPEkWp.png">
<br>
<b>Phone:</b> <img src="https://i.imgur.com/1Z1rgr1.png">
<br>
We do this by adding one more media query (at 600px), and a set of new classes for devices larger than 600px (but smaller than 768px):
<pre>
/* For mobile phones: */
[class*="col-"] {
  width: 100%;
}
@media only screen and (min-width: 600px) {
  /* For tablets: */
  .col-s-1{width:8.33%;}
  .col-s-2{width:16.66%;}
  .col-s-3{width:25%;}
  .col-s-4{width:33.33%;}
  .col-s-5{width:41.66%;}
  .col-s-6{width:50%;}
  .col-s-7{width:58.33%;}
  .col-s-8{width:66.66%;}
  .col-s-9{width:75%;}
  .col-s-10{width:83.33%;}
  .col-s-11{width:91.66%;}
  .col-s-12{width:100%;}
}
@media only screen and (min-width: 768px) {
  /* For desktop: */
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
}
</pre>
It might seem odd that we have two sets of identical classes, but it gives us the opportunity in HTML, to decide what will happen with the columns at each breakpoint:
<pre>
&lt;div class="row"&gt;
  &lt;div class="col-3 col-s-3"&gt;...&lt;/div&gt;
  &lt;div class="col-6 col-s-9"&gt;...&lt;/div&gt;
  &lt;div class="col-3 col-s-12"&gt;...&lt;/div&gt;
&lt;/div&gt;
</pre>
There are tons of screens and devices with different heights and widths, so it is hard to create an exact breakpoint for each device. To keep things simple you could target five groups:
<pre>
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {...}
/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {...}
/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {...}
/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {...}
/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {...}
</pre>
<h1>Orientation</h1>
Media queries can also be used to change layout of a page depending on the orientation of the browser.
<br>
You can have a set of CSS properties that will only apply when the browser window is wider than its height, a so called "Landscape" orientation:
<pre>
@media only screen and (orientation: landscape) {
  body {
    background-color: lightblue;
  }
}
</pre>
<h1>Hide Elements With Media Queries</h1>
Another common use of media queries, is to hide elements on different screen sizes:
<pre>
/* If the screen size is 600px wide or less, hide the element */
@media only screen and (max-width: 600px) {
  div.example {
    display: none;
  }
}
</pre>
<h1>Change Font Size With Media Queries</h1>
You can also use media queries to change the font size of an element on different screen sizes:
<pre>
/* If the screen size is 601px or more, set the font-size of &lt;div&gt; to 80px */
@media only screen and (min-width: 601px) {
  div.example {
    font-size: 80px;
  }
}
/* If the screen size is 600px or less, set the font-size of &lt;div&gt; to 30px */
@media only screen and (max-width: 600px) {
  div.example {
    font-size: 30px;
  }
}
</pre>
