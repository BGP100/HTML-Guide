HTML links can be used to create bookmarks, so that readers can jump to specific parts of a web page.
<br>
Bookmarks can be useful if a web page is very long.
<br>
To create a bookmark - first create the bookmark, then add a link to it.
<br>
When the link is clicked, the page will scroll down or up to the location with the bookmark.
<br>
First, use the id attribute to create a bookmark:
<pre>&lt;h2 id="C4"&gt;Chapter 4&lt;/h2&gt;</pre>
Then, add a link to the bookmark ("Jump to Chapter 4"), from within the same page:
<pre>&lt;a href="#C4"&gt;Jump to Chapter 4&lt;/a&gt;</pre>
You can also add a link to a bookmark on another page:
<pre>&lt;a href="../Bookmarks.md#C4"&gt;Jump to Chapter 4&lt;/a&gt;</pre>
