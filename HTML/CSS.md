CSS stands for Cascading Style Sheets.
<br>
CSS saves a lot of work. It can control the layout of multiple web pages all at once.
<br>
<img src="https://i.imgur.com/ykGRquA_d.webp?maxwidth=450&shape=thumb&fidelity=medium">
<h1>What is it</h1>
Cascading Style Sheets (CSS) is used to format the layout of a webpage.
<br>
With CSS, you can control the color, font, the size of text, the spacing between elements, how elements are positioned and laid out, what background images or background colors are to be used, different displays for different devices and screen sizes, and much more!
<br>
<b>Tip:</b> The word cascading means that a style applied to a parent element will also apply to all children elements within the parent. So, if you set the color of the body text to "blue", all headings, paragraphs, and other text elements within the body will also get the same color (unless you specify something else)!
<h1>How is used</h1>
CSS can be added to HTML documents in 3 ways:
<ul>
  <li>Inline - by using the style attribute inside HTML elements.</li>
  <li>Internal - by using a &lt;style&gt; element in the &lt;head&gt; section.</li>
  <li>External - by using a &lt;link&gt; element to link to an external CSS file.</li>
</ul>
The most common way to add CSS, is to keep the styles in external CSS files. However, in this tutorial we will use inline and internal styles, because this is easier to demonstrate, and easier for you to try it yourself.
<h1>Inline</h1>
An inline CSS is used to apply a unique style to a single HTML element.
<br>
An inline CSS uses the style attribute of an HTML element.
<br>
The following example sets the text color of the &lt;h1&gt; element to blue, and the text color of the &lt;p&gt; element to red:
<pre>
&lt;h1 style="color:blue;"&gt;A Blue Heading&lt;/h1&gt;

&lt;p style="color:red;"&gt;A red paragraph.&lt;/p&gt;
</pre>
<h1>Internal</h1>
An internal CSS is used to define a style for a single HTML page.
<br>
An internal CSS is defined in the <head> section of an HTML page, within a <style> element.
<br>
The following example sets the text color of ALL the &lt;h1&gt; elements (on that page) to blue, and the text color of ALL the &lt;p&gt; elements to red. In addition, the page will be displayed with a "powderblue" background color:
<pre>
&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;style&gt;
      body {background-color: powderblue;}
      h1 {color: blue;}
      p {color: red;}
    &lt;/style&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;This is a heading&lt;/h1&gt;
    &lt;p&gt;This is a paragraph.&lt;/p&gt;
  &lt;/body&gt;
&lt;/html&gt;
</pre>
<h1>External</h1>
An external style sheet is used to define the style for many HTML pages.
<br>
To use an external style sheet, add a link to it in the <head> section of each HTML page:
<b>HTML:</b>
<pre>
&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;link rel="stylesheet" href="styles.css"&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;This is a heading&lt;/h1&gt;
    &lt;p&gt;This is a paragraph.&lt;/p&gt;
  &lt;/body&gt;
&lt;/html&gt;
</pre>
<b>CSS:</b>
<pre>
body {
  background-color: powderblue;
}
h1 {
  color: blue;
}
p {
  color: red;
}
</pre>
<h1>Colors, Fonts & Sizes</h1>
Here, we will demonstrate some commonly used CSS properties. You will learn more about them later.
<br>
The CSS color property defines the text color to be used.
<br>
The CSS font-family property defines the font to be used.
<br>
The CSS font-size property defines the text size to be used.
<pre>
h1 {
  color: blue;
  font-family: verdana;
  font-size: 300%;
}
p {
  color: red;
  font-family: courier;
  font-size: 160%;
}
</pre>
<h1>Border</h1>
The CSS border property defines a border around an HTML element.
<pre>
p {
  border: 2px solid powderblue;
}
</pre>
<h1>Padding</h1>
The CSS padding property defines a padding (space) between the text and the border.
<pre>
p {
  border: 2px solid powderblue;
  padding: 30px;
}
</pre>
<h1>Margin</h1>
The CSS padding property defines a padding (space) between the text and the border.
<pre>
p {
  border: 2px solid powderblue;
  margin: 50px;
}
</pre>
<h1>Link External</h1>
External style sheets can be referenced with a full URL or with a path relative to the current web page.
<pre>&lt;link rel="stylesheet" href="https://www.w3schools.com/html/styles.css"&gt;</pre>
