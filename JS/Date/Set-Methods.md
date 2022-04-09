Set Date methods are used for setting a part of a date:
<ul>
  <li><a href="#setDate">setDate()</a></li>
  <li><a href="#setFullYear">setFullYear()</a></li>
  <li><a href="#setHours">setHours()</a></li>
  <li><a href="#setMinutes">setMinutes()</a></li>
  <li><a href="#setMonth">setMonth()</a></li>
  <li><a href="#setSeconds">setSeconds()</a></li>
</ul>
<h1>setFullYear()</h1>
The <b>setFullYear()</b> method sets the year of a date object. In this example to 2020:
<pre>
const d = new Date();
d.setFullYear(2020);
</pre>
The <b>setFullYear()</b> method can optionally set month and day:
<pre>
const d = new Date();
d.setFullYear(2020, 11, 3);
</pre>
<h1>setMonth()</h1>
The <b>setMonth()</b> method sets the month of a date object (0-11):
<pre>
const d = new Date();
d.setMonth(11);
</pre>
<h1>setDate()</h1>
The <b>setDate()</b> method sets the day of a date object (1-31):
<pre>
const d = new Date();
d.setDate(15);
</pre>
The <b>setDate()</b> method can also be used to add days to a date:
<pre>
const d = new Date();
d.setDate(d.getDate() + 50);
</pre>
If adding days shifts the month or year, the changes are handled automatically by the Date object.
<h1>setHours()</h1>
The <b>setHours()</b> method sets the hours of a date object (0-23):
<pre>
const d = new Date();
d.setHours(22);
</pre>
<h1>setMinutes()</h1>
The <b>setMinutes()</b> method sets the minutes of a date object (0-59):
<pre>
const d = new Date();
d.setMinutes(30);
</pre>
<h1>setSeconds()</h1>
The <b>setSeconds()</b> method sets the seconds of a date object (0-59):
<pre>
const d = new Date();
d.setSeconds(30);
</pre>
