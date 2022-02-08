I don't know what to put here...
<br>
Just copy the code:
<h2>CSS:</h2>
<pre>
@charset "UTF-8";

article, aside, footer, header, main, nav, section {
  display: block;
}

html, body, h1, h2, h3, ul, li, a, p, 
article, aside, footer, header, main, nav, section {
  padding: 0;
  margin: 0;
}

.banner {
  background-color: #11233b;
  color: white;
  padding: 10px 20px;
}

body {
  width: 960px;
  margin-left: auto;
  margin-right: auto;
  background-color: #f0f0f0;
  font-family: Helvetica, Arial, sans-serif;
  font-size: 15px;
}

nav {
  background-color: #20416c;
  padding: 5px;
  margin-top: 1px;
}

li a {
  color: white;
}

li {
  display: inline;
  margin-left: 15px;
  margin-right: 15px;
  font-size: 20px;
  font-variant: small-caps;
  font-weight: bold;
}

section {
  background-color: #bbbbbb;
  margin-top: 10px;
  padding: 5px;
}

article {
  background-color: white;
  margin-top: 5px;
  padding: 10px 15px;
}

main {
  width: 640px;
  float: left;
  margin-bottom: 10px;
}

aside {
  background-color: #bbbbbb;
  width: 270px;
  float: right;
  padding: 20px;
  margin-top: 10px;
}

footer {
  clear: both;
  background-color: #20416c;
  color: white;
  padding: 5px 20px;
}
</pre>
<h2>HTML:</h2>
<pre>
&lt;!DOCTYPE html&gt;
&lt;html lang="en"&gt;
  &lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;title>News&lt;/title&gt;
    &lt;link rel="stylesheet" type="text/css" href="style.css"&gt;
    &lt;!--[if lt IE 9]&gt;
    &lt;script&gt;
      document.createElement("article");
      document.createElement("aside");
      document.createElement("footer");
      document.createElement("header");
      document.createElement("main");
      document.createElement("nav");
      document.createElement("section");
    &lt;/script&gt;
    &lt;![endif]--&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;header class="banner"&gt;
      &lt;h1&gt;News&lt;/h1&gt;
      &lt;p&gt;Local and National News&lt;/p&gt;
    &lt;/header&gt;
    &lt;nav&gt;
      &lt;ul&gt;
        &lt;li>&lt;a href="index.html">Home&lt;/a>&lt;/li&gt;
        &lt;li>&lt;a href="archive.html">Archives&lt;/a>&lt;/li&gt;
        &lt;li>&lt;a href="about.html">About&lt;/a>&lt;/li&gt;
      &lt;/ul&gt;
    &lt;/nav&gt;
    &lt;main&gt;
      &lt;section&gt;
        &lt;h2&gt;Local News&lt;/h2&gt;
        &lt;article&gt;
          &lt;header&gt;
            &lt;h3&gt;Fire fighters rescue man from building&lt;/h3&gt;
            &lt;p&gt;(author, date)&lt;/p&gt;
          &lt;/header>
          &lt;p&gt;This is the story text. This is the story text.&lt;/p&gt;
          &lt;p&gt;This is the story text. This is the story text.&lt;/p&gt;
        &lt;/article&gt;
        &lt;article&gt;
          &lt;header&gt;
            &lt;h3&gt;New Library to be built&lt;/h3&gt;
            &lt;p&gt;(author, date)&lt;/p&gt;
          &lt;/header&gt;
          &lt;p&gt;This is the story text. This is the story text.&lt;/p&gt;
          &lt;p&gt;This is the story text. This is the story text.&lt;/p&gt;
        &lt;/article&gt;
      &lt;/section&gt;
      &lt;section&gt;
        &lt;h2&gt;National News&lt;/h2&gt;
        &lt;article&gt;
          &lt;header&gt;
            &lt;h3&gt;Snow storm is making travel difficult&lt;/h3&gt;
            &lt;p&gt;(author, date)&lt;/p&gt;
          &lt;/header&gt;
          &lt;p&gt;This is the story text. This is the story text.&lt;/p&gt;
          &lt;p&gt;This is the story text. This is the story text.&lt;/p&gt;
        &lt;/article&gt;
        &lt;article&gt;
          &lt;header&gt;
            &lt;h3&gt;Thousands are without power&lt;/h3&gt;
            &lt;p&gt;(author, date)&lt;/p&gt;
          &lt;/header&gt;
          &lt;p&gt;This is the story text. This is the story text.&lt;/p&gt;
          &lt;p&gt;This is the story text. This is the story text.&lt;/p&gt;
        &lt;/article&gt;
      &lt;/section&gt;
    &lt;/main&gt;
    &lt;aside&gt;
      &lt;h2&gt;Be a news reporter&lt;/h2&gt;
      &lt;p&gt;If you see news happening - Send us a Text.&lt;/p&gt;
    &lt;/aside&gt;
    &lt;footer&gt;
      &lt;p&gt;Footer Information&lt;/p&gt;
    &lt;/footer&gt;
  &lt;/body&gt;
&lt;/html&gt;
</pre>
