<img src="https://i.imgur.com/qhewgGc.jpg" width="69%">
<br>
CSS counters are "variables" maintained by CSS whose values can be incremented by CSS rules (to track how many times they are used). Counters let you adjust the appearance of content based on its placement in the document.
<h1>Automatic Numbering</h1>
CSS counters are like "variables". The variable values can be incremented by CSS rules (which will track how many times they are used).
<br>
To work with CSS counters we will use the following properties:
<ul>
  <li><b>counter-reset</b> - Creates or resets a counter</li>
  <li><b>counter-increment</b> - Increments a counter value</li>
  <li><b>content</b> - Inserts generated content</li>
  <li><b>counter()</b> or <b>counters()</b> function - Adds the value of a counter to an element</li>
</ul>
To use a CSS counter, it must first be created with counter-reset.
<br>
The following example creates a counter for the page (in the body selector), then increments the counter value for each <b>&lt;h2&gt;</b> element and adds "Section <i>&lt;value of the counter&gt;</i>:" to the beginning of each <b>&lt;h2&gt;</b> element:
<pre>
body {
  counter-reset: section;
}
h2::before {
  counter-increment: section;
  content: "Section " counter(section) ": ";
}
</pre>
<h1>Nesting Counters</h1>
The following example creates one counter for the page (section) and one counter for each <b>&lt;h1&gt;</b> element (subsection). The "section" counter will be counted for each <b>&lt;h1&gt;</b> element with "Section <i>&lt;value of the section counter&gt;</i>.", and the "subsection" counter will be counted for each <b>&lt;h2&gt;</b> element with "<i>&lt;value of the section counter&gt;</i>.<i>&lt;value of the subsection counter&gt;</i>":
<pre>
body {
  counter-reset: section;
}
h1 {
  counter-reset: subsection;
}
h1::before {
  counter-increment: section;
  content: "Section " counter(section) ". ";
}
h2::before {
  counter-increment: subsection;
  content: counter(section) "." counter(subsection) " ";
}
</pre>
A counter can also be useful to make outlined lists because a new instance of a counter is automatically created in child elements. Here we use the <b>counters()</b> function to insert a string between different levels of nested counters:
<pre>
ol {
  counter-reset: section;
  list-style-type: none;
}
li::before {
  counter-increment: section;
  content: counters(section,".") " ";
}
</pre>
