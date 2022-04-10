<a href="/CSS/Units.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/CSS/!important.md">Next &gt;</a>
<hr>
<h1>What is it?</h1>
If there are two or more CSS rules that point to the same element, the selector with the highest specificity value will "win", and its style declaration will be applied to that HTML element.
<br>
Think of specificity as a score/rank that determines which style declaration are ultimately applied to an element.
<br>
Look at the following examples:
<pre>
&lt;style&gt;
  p{color:red;}
&lt;/style&gt;
&lt;p&gt;Hello World!&lt;/p&gt;
</pre>
Now, let's look at another example:
<pre>
&lt;style&gt;
  .test{color:green;}
  p{color:red;}
&lt;/style&gt;
&lt;p class="test"&gt;Hello World!&lt;/p&gt;
</pre>
AND, another example:
<pre>
&lt;style&gt;
  #demo{color:blue;}
  .test{color:green;}
  p{color:red;}
&lt;/style&gt;
&lt;p id="demo" class="test"&gt;Hello World!&lt;/p&gt;
</pre>
Last example:
<pre>
&lt;style&gt;
  #demo{color:blue;}
  .test{color:green;}
  p{color:red;}
&lt;/style&gt;
&lt;p id="demo" class="test" style="color:pink;"&gt;Hello World!&lt;/p&gt;
</pre>
<h1>Hierarchy</h1>
Every CSS selector has its place in the specificity hierarchy.
<br>
There are four categories which define the specificity level of a selector:
<ul>
  <li><b>Inline styles</b> - Example: &lt;h1 style="color: pink;"&gt;</li>
  <li><b>IDs</b> - Example: #navbar</li>
  <li><b>Classes, pseudo-classes, attribute selectors</b> - Example: .test, :hover, [href]</li>
  <li><b>Elements and pseudo-elements</b> - Example: h1, :before</li>
</ul>
<h1>How to Calculate it?</h1>
Memorize how to calculate specificity!
<br>
Start at 0, add 100 for each ID value, add 10 for each class value (or pseudo-class or attribute selector), add 1 for each element selector or pseudo-element.
<br>
<b>Note:</b> Inline style gets a specificity value of 1000, and is always given the highest priority!
<br>
<b>Note 2:</b> There is one exception to this rule: if you use the <a href="!important.md">!important</a> rule, it will even override inline styles!
<br>
The table below shows some examples on how to calculate specificity values:
<table class="ws-table-all notranslate">
  <tr>
    <th>Selector</th>
    <th>Specificity Value</th>
    <th>Calculation</th>
  </tr>
  <tr>
    <td>p</td>
    <td>1</td>
    <td>1</td>
  </tr>
  <tr>
    <td>p.test</td>
    <td>11</td>
    <td>1+10</td>
  </tr>
  <tr>
    <td>p#demo</td>
    <td>101</td>
    <td>1+100</td>
  </tr>
  <tr>
    <td>&lt;p style="color:pink;"&gt;</td>
    <td>1000</td>
    <td>1000</td>
  </tr>
  <tr>
    <td>#demo</td>
    <td>100</td>
    <td>100</td>
  </tr>
  <tr>
    <td>.test</td>
    <td>10</td>
    <td>10</td>
  </tr>
  <tr>
    <td>p.test1.test2</td>
    <td>21</td>
    <td>1+10+10</td>
  </tr>
  <tr>
    <td>#navbar p#demo</td>
    <td>201</td>
    <td>100+1+100</td>
  </tr>
  <tr>
    <td>*</td>
    <td>0</td>
    <td>0 (the universal selector is ignored)</td>
  </tr>
</table>
<b>The selector with the highest specificity value will win and take effect!</b>
<br>
Consider these three code fragments:
<pre>A: h1</pre>
<pre>B: h1#content</pre>
<pre>C: &lt;h1 id="content" style="color: pink;"&gt;Heading&lt;/h1&gt;</pre>
<ul>
  <li>The specificity of A is 1 (one element selector)</li>
  <li>The specificity of B is 101 (one ID reference + one element selector)</li>
  <li>The specificity of C is 1000 (inline styling)</li>
</ul>
Since the third rule (C) has the highest specificity value (1000), this style declaration will be applied.
<h1>More Examples</h1>
<pre>
h1 {background-color: yellow;}
h1 {background-color: red;}
</pre>
<hr>
<pre>
div#a {background-color: green;}
#a {background-color: yellow;}
div[id=a] {background-color: blue;}
</pre>
<hr>
<pre>
#content h1.red {background-color: red;}
#content h1.yellow {background-color: yellow;}
</pre>
<hr>
<pre>
.intro {background-color: yellow;}
h1 {background-color: red;}
</pre>
