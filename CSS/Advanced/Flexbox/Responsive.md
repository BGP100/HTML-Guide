<a href="/CSS/Advanced/Flexbox/Items.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="https://bledy-guides.repl.co/#css3">Next &gt;</a>
<hr>
You learned from the CSS <a href="https://github.com/BGP100/HTML-Guide/blob/main/CSS/Advanced/MediaQueries.md">Media Queries</a> chapter that you can use media queries to create different layouts for different screen sizes and devices.
<br>
For example, if you want to create a two-column layout for most screen sizes, and a one-column layout for small screen sizes (such as phones and tablets), you can change the <b>flex-direction</b> from <b>row</b> to <b>column</b> at a specific breakpoint (800px in the example below):
<pre>
.flex-container {
  display: flex;
  flex-direction: row;
}
/* Responsive layout - makes a one column layout instead of a two-column layout */
@media (max-width: 800px) {
  .flex-container {
    flex-direction: column;
  }
}
</pre>
Another way is to change the percentage of the <b>flex</b> property of the flex items to create different layouts for different screen sizes. Note that we also have to include <b>flex-wrap: wrap;</b> on the flex container for this example to work:
<pre>
.flex-container {
  display: flex;
  flex-wrap: wrap;
}
.flex-item-left {
  flex: 50%;
}
.flex-item-right {
  flex: 50%;
}
/* Responsive layout - makes a one column layout instead of a two-column layout */
@media (max-width: 800px) {
  .flex-item-right, .flex-item-left {
    flex: 100%;
  }
}
</pre>
