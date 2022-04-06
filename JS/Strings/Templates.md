Synonyms:
<ul>
  <li>Template Literals</li>
  <li>Template Strings</li>
  <li>String Templates</li>
  <li>Back-Tics Syntax</li>
</ul>
<h1>Browser Support</h1>
<table class="ws-table-all notranslate">
  <tr>
    <th>Browser</th>
    <th>Chrome</th>
    <th>Edge</th>
    <th>Firefox</th>
    <th>Safari</th>
    <th>Opera</th>
  </tr>
  <tr>
    <td>Compatibility</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
    <td>Yes</td>
  </tr>
</table>
<h1>Back-Tics Syntax</h1>
Template Literals use back-ticks (<code>``</code>) rather than the quotes (<code>""</code>) to define a string:
<pre>let text = `Hello World!`;</pre>
<h2>Quotes Inside Back-Tics</h2>
With template literals, you can use both single and double quotes inside a string:
<pre>let text = `He's often called "Johnny"`;</pre>
<h2>Multiple Lines</h2>
Template literals allows multiline strings:
<pre>
let text =
`The quick
brown fox
jumps over
the lazy dog`;
</pre>
<h2>Variable Substitutions</h2>
Template literals allow variables in strings:
<pre>
let firstName = "John";
let lastName = "Doe";
let text = `Welcome ${firstName}, ${lastName}!`;
</pre>
<pre>
let price = 10;
let VAT = 0.25;
let total = `Total: ${(price * (1 + VAT)).toFixed(2)}`;
</pre>
<h1>Example</h1>
<pre>
let header = "Templates Literals";
let tags = ["template literals", "javascript", "es6"];
let html = `&lt;h2&gt;${header}&lt;/h2&gt;&lt;ul&gt;`; 
for (const x of tags) {
  html += `&lt;li&gt;${x}&lt;/li&gt;`;
}
html += `&lt;/ul&gt;`;
</pre>
