<a href="/HTML/Formats.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/Comments.md">Next &gt;</a>
<hr>
<ul>
  <li><a href="#blockquote">&lt;blockquote&gt;</a></li>
  <li><a href="#q">&lt;q&gt;</a></li>
  <li><a href="#abbr">&lt;abbr&gt;</a></li>
  <li><a href="#address">&lt;address&gt;</a></li>
  <li><a href="#cite">&lt;cite&gt;</a></li>
  <li><a href="#bdo">&lt;bdo&gt;</a></li>
</ul>
<h1>&lt;blockquote&gt;</h1>
The HTML <b>&lt;blockquote&gt;</b> element defines a section that is quoted from another source.
<br>
Browsers usually indent <b>&lt;blockquote&gt;</b> elements.
<h2>Preview:</h2>
<p>Here is a quote from WWF's website:</p>
<blockquote cite="http://www.worldwildlife.org/about">
For 50 years, WWF has been protecting the future of nature.
The world's leading conservation organization,
WWF works in 100 countries and is supported by
1.2 million members in the United States and
close to 5 million globally.
</blockquote>
<h2>Demo:</h2>
<pre>
&lt;p&gt;Browsers usually indent blockquote elements.&lt;/p&gt;
<p></p>
&lt;blockquote cite="//www.worldwildlife.org/about"&gt;
For 50 years, WWF has been protecting the future of nature.
The world's leading conservation organization,
WWF works in 100 countries and is supported by
1.2 million members in the United States and
close to 5 million globally.
&lt;/blockquote&gt;
</pre>
<h1>&lt;q&gt;</h1>
The HTML <b>&lt;q&gt;</b> tag defines a short quotation.
<br>
Browsers normally insert quotation marks around the quotation.
<h2>Preview:</h2>
<p>WWF's goal is to: <q>Build a future where people live in harmony with nature.</q></p>
<h2>Demo:</h2>
<pre>&lt;p&gt;WWF's goal is to: <q>Build a future where people live in harmony with nature.&lt;/q&gt;&lt;/p&gt;</pre>
<h1>&lt;abbr&gt;</h1>
The HTML <b>&lt;abbr&gt;</b> tag defines an abbreviation or an acronym, like "HTML", "CSS", "Mr.", "Dr.", "ASAP", "ATM".
<br>
Marking abbreviations can give useful information to browsers, translation systems and search-engines.
<h2>Preview:</h2>
<p>The <abbr title="World Health Organization">WHO</abbr> was founded in 1948.</p>
<p>Marking up abbreviations can give useful information to browsers, translation systems and search-engines.</p>
<h2>Demo:</h2>
<pre>
&lt;p&gt;The &lt;abbr title="World Health Organization"&gt;WHO</abbr> was founded in 1948.&lt;/p&gt;
&lt;p&gt;Marking up abbreviations can give useful information to browsers, translation systems and search-engines.&lt;/p&gt;
</pre>
<h1>&lt;address&gt;</h1>
The HTML <b>&lt;address&gt;</b> tag defines the contact information for the author/owner of a document or an article.
<br>
The contact information can be an email address, URL, physical address, phone number, social media handle, etc.
<br>
The text in the <b>&lt;address&gt;</b> element usually renders in italic, and browsers will always add a line break before and after the <b>&lt;address&gt;</b> element.
<h2>Preview:</h2>
<p>The HTML address element defines contact information (author/owner) of a document or article.</p>
<address>
Written by John Doe.
<br> 
Visit us at:
<br>
Example.com
<br>
Box 564, Disneyland
<br>
USA
</address>
<p></p>
Yeah, in github this doesn't work...
<h2>Demo:</h2>
<pre>
&lt;p&gt;The HTML address element defines contact information (author/owner) of a document or article.&lt;/p&gt;
&lt;address&gt;
Written by John Doe.&lt;br&gt; 
Visit us at:&lt;br&gt;
Example.com&lt;br&gt;
Box 564, Disneyland&lt;br&gt;
USA
&lt;/address&gt;
</pre>
<h1>&lt;cite&gt;</h1>
The HTML <b>&lt;cite&gt;</b> tag defines the title of a creative work. (e.g. a book, a poem, a song, a movie, a painting, a sculpture, etc.)
<br>
<b>Note:</b> A person's name is not the title of a work.
<br>
The text in the <b>&lt;cite&gt;</b> element usually renders in italic.
<h2>Preview:</h2>
The HTML <b>cite</b> element defines the title of a work.
<br>
Browsers usually display cite elements in italic.
<p></p>
<img src="https://www.w3schools.com/html/img_the_scream.jpg" width="220" height="277" alt="The Scream">
<p><cite>The Scream</cite> by Edvard Munch. Painted in 1893.</p>
<h2>Demo:</h2>
<pre>
The HTML cite element defines the title of a work.&lt;br&gt;
&lt;p&gt;Browsers usually display cite elements in italic.&lt;/p&gt;
&lt;img src="//www.w3schools.com/html/img_the_scream.jpg" width="220" height="277" alt="The Scream"&gt;
&lt;p&gt;&lt;cite&gt;The Scream&lt;/cite&gt; by Edvard Munch. Painted in 1893.&lt;/p&gt;
</pre>
<h1>&lt;bdo&gt;</h1>
BDO stands for Bi-Directional Override.
<br>
The HTML <bdo> tag is used to override the current text direction:
<h2>Preview:</h2>
<p>If your browser supports bi-directional override (bdo), the next line will be written from right to left (rtl):</p>
<br>
tfel ot thgir morf nettirw eb lliw enil sihT
<h2>Demo:</h2>
<pre>
&lt;p&gt;If your browser supports bi-directional override (bdo), the next line will be written from right to left (rtl):&lt;/p&gt;
&lt;br&gt;
&lt;bdo dir="rtl">This line will be written from right to left.&lt;/bdo&gt;
</pre>
