<a href="/CSS/Display.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/Posistion.md">Next &gt;</a>
<hr>
As mentioned in the <a href="Display.md">previous chapter</a>; a block-level element always takes up the full width available (stretches out to the left and right as far as it can).
<br>
Setting the <b>width</b> of a block-level element will prevent it from stretching out to the edges of its container. Then, you can set the margins to auto, to horizontally center the element within its container. The element will take up the specified width, and the remaining space will be split equally between the two margins.
<hr>
<b><i>Note:</i></b> The problem with the <b>&lt;div&gt;</b> above occurs when the browser window is smaller than the width of the element. The browser then adds a horizontal scrollbar to the page.
<br>
Using <b>max-width</b> instead, in this situation, will improve the browser's handling of small windows. This is important when making a site usable on small devices:
<hr>
<b><i>Tip:</i></b> Resize the browser window to less than 500px wide, to see the difference between the two divs!
<br>
Here is an example of the two divs above:
<pre>
div.ex1 {
  width: 500px;
  margin: auto;
  border: 3px solid #73AD21;
}
div.ex2 {
  max-width: 500px;
  margin: auto;
  border: 3px solid #73AD21;
}
</pre>
