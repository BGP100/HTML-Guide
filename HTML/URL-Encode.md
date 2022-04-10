<a href="/HTML/Charset.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/HTML/XHTML.md">Next &gt;</a>
<hr>
A URL is another word for a web address.
<br>
A URL can be composed of words (e.g. w3schools.com), or an Internet Protocol (IP) address (e.g. 192.68.20.50).
<br>
Most people enter the name when surfing, because names are easier to remember than numbers.
<hr>
Web browsers request pages from web servers by using a URL.
<br>
A Uniform Resource Locator (URL) is used to address a document (or other data) on the web.
<br>
A web address like https://preview.bledygamesweb.repl.co follows these syntax rules:
<pre>scheme://prefix.domain:port/path/filename</pre>
<b>Explanation:</b>
<ul>
  <li>scheme - defines the <i>type</i> of Internet service (most common is <i>http or https</i>)</li>
  <li>prefix - defines a domain <i>prefix</i> (default for http is <i>www</i>)</li>
  <li>domain - defines the Internet <b>domain name </b>(like w3schools.com)</li>
  <li>port - defines the <i>port number</i> at the host (default for http is <i>80</i>)</li>
  <li>path - defines a <i>path</i> at the server (If omitted: the root directory of the site)</li>
  <li>filename - defines the name of a document or resource</li>
</ul>
<h1>URL Schemes</h1>
The table below lists some common schemes:
<table class="ws-table-all notranslate">
  <tr>
    <th>Scheme</th>
    <th>Short for</th>
    <th>Used for</th>
  </tr>
  <tr>
    <td>http</td>
    <td>HyperText Transfer Protocol</td>
    <td>Common web pages. Not encrypted</td>
  </tr>
  <tr>
    <td>https</td>
    <td>Secure HyperText Transfer Protocol</td>
    <td>Secure web pages. Encrypted</td>
  </tr>
  <tr>
    <td>ftp</td>
    <td>File Transfer Protocol</td>
    <td>Downloading or uploading files</td>
  </tr>
  <tr>
    <td>file</td>
    <td>-</td>
    <td>A file on your computer</td>
  </tr>
</table>
<h1>ASCII URL Encoding</h1>
URLs can only be sent over the Internet using the ASCII character-set. If a URL contains characters outside the ASCII set, the URL has to be converted.
<br>
URL encoding converts non-ASCII characters into a format that can be transmitted over the Internet.
<br>
URL encoding replaces non-ASCII characters with a "%" followed by hexadecimal digits.
<br>
URLs cannot contain spaces. URL encoding normally replaces a space with a plus (+) sign, or %20.
<pre>
&lt;form name="input" target="_blank" action="/action_page2.php" method="get"&gt;
  &lt;input type="text" value="Hello Günter" name="text" size="30"&gt;
  &lt;input type="submit" value="Submit"&gt;
&lt;/form&gt;
</pre>
If you click "Submit", the browser will URL encode the input before it is sent to the server.
<br>
A page at the server will display the received input.
<br>
Try some other input and click Submit again.
<h1>ASCII Encoding Examples</h1>
Your browser will encode input, according to the character-set used in your page.
<br>
The default character-set in HTML5 is UTF-8.
<p></p>
<table class="ws-table-all notranslate">
  <tr>
    <th style="width:20%">Character</th>
    <th style="width:40%">From Windows-1252</th>
    <th style="width:40%">From UTF-8</th>
    </tr>
  <tr>
    <td>€</td>
    <td>%80</td>
    <td>%E2%82%AC</td>
  </tr>
  <tr>
    <td>£</td>
    <td>%A3</td>
    <td>%C2%A3</td>
  </tr>
  <tr>
    <td>©</td>
    <td>%A9</td>
    <td>%C2%A9</td>
  </tr>
  <tr>
    <td>®</td>
    <td>%AE</td>
    <td>%C2%AE</td>
  </tr>
  <tr>
    <td>À</td>
    <td>%C0</td>
    <td>%C3%80</td>
  </tr>
  <tr>
    <td>Á</td>
    <td>%C1</td>
    <td>%C3%81</td>
  </tr>
  <tr>
    <td>Â</td>
    <td>%C2</td>
    <td>%C3%82</td>
  </tr>
  <tr>
    <td>Ã</td>
    <td>%C3</td>
    <td>%C3%83</td>
  </tr>
  <tr>
    <td>Ä</td>
    <td>%C4</td>
    <td>%C3%84</td>
  </tr>
  <tr>
    <td>Å</td>
    <td>%C5</td>
    <td>%C3%85</td>
  </tr>
</table>
