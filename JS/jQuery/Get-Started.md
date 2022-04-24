<h1>Adding jQuery to Your Web Pages</h1>
There are several ways to start using jQuery on your web site. You can:
<ul>
  <li>Download the jQuery library from jQuery.com</li>
  <li>Include jQuery from a CDN, like Google</li>
</ul>
<h1>Downloading jQuery</h1>
There are two versions of jQuery available for downloading:
<ul>
  <li>Production version - this is for your live website because it has been minified and compressed</li>
  <li>Development version - this is for testing and development (uncompressed and readable code)</li>
</ul>
Both versions can be downloaded from jQuery.com.
<br>
The jQuery library is a single JavaScript file, and you reference it with the HTML <b>&lt;script&gt;</b> tag (notice that the <b>&lt;script&gt;</b> tag should be inside the <b>&lt;head&gt;</b> section):
<pre>
&lt;head&gt;
&lt;script src="jquery-3.6.0.min.js"&gt;&lt;/script&gt;
&lt;/head&gt;
</pre>
<b>Tip:</b> Place the downloaded file in the same directory as the pages where you wish to use it.
<h1>CDN</h1>
If you don't want to download and host jQuery yourself, you can include it from a CDN (Content Delivery Network).
<br>
Google is an example of someone who host jQuery:
<pre>
&lt;head&gt;
&lt;script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"&gt;&lt;/script&gt;
&lt;/head&gt;
</pre>
<b>One big advantage of using the hosted jQuery from Google:</b>
<br>
Many users already have downloaded jQuery from Google when visiting another site. As a result, it will be loaded from cache when they visit your site, which leads to faster loading time. Also, most CDN's will make sure that once a user requests a file from it, it will be served from the server closest to them, which also leads to faster loading time.
