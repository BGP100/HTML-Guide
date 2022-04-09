These methods can be used for getting information from a date object:
<ul>
  <li><a href="#getTime">getTime()</a></li>
  <li><a href="#getFullYear">getFullYear()</a></li>
  <li><a href="#getMonth">getMonth()</a></li>
  <li><a href="#getDate">getDate()</a></li>
  <li><a href="#getHours">getHours()</a></li>
  <li><a href="#getMinutes">getMinutes()</a></li>
  <li><a href="#getSeconds">getSeconds()</a></li>
  <li><a href="#getMilliseconds">getMilliseconds()</a></li>
  <li><a href="#getDay">getDay()</a></li>
</ul>
<h1>getTime()</h1>
The <b>getTime()</b> method returns the number of milliseconds since January 1, 1970:
<pre>
const d = new Date();
d.getTime();
</pre>
<h1>getFullYear()</h1>
The <b>getFullYear()</b> method returns the year of a date as a four digit number:
<pre>
const d = new Date();
d.getFullYear();
</pre>
<h1>getMonth()</h1>
The <b>getMonth()</b> method returns the month of a date as a number (0-11):
<pre>
const d = new Date();
d.getMonth();
</pre>
In JavaScript, the first month (January) is month number 0, so December returns month number 11.
<br>
You can use an array of names, and <b>getMonth()</b> to return the month as a name:
<pre>
const months = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"];
const d = new Date();
let month = months[d.getMonth()];
</pre>
<h1>getDate()</h1>
The <b>getDate()</b> method returns the day of a date as a number (1-31):
<pre>
const d = new Date();
d.getDate();
</pre>
<h1>getHours()</h1>
The <b>getHours()</b> method returns the hours of a date as a number (0-23):
<pre>
const d = new Date();
d.getHours();
</pre>
<h1>getMinutes()</h1>
The <b>getMinutes()</b> method returns the minutes of a date as a number (0-59):
<pre>
const d = new Date();
d.getMinutes();
</pre>
<h1>getSeconds()</h1>
The <b>getSeconds()</b> method returns the seconds of a date as a number (0-59):
<pre>
const d = new Date();
d.getSeconds();
</pre>
<h1>getMilliseconds()</h1>
The <b>getMilliseconds()</b> method returns the milliseconds of a date as a number (0-999):
<pre>
const d = new Date();
d.getMilliseconds();
</pre>
<h1>getDay()</h1>
The <b>getDay()</b> method returns the weekday of a date as a number (0-6):
<pre>
const d = new Date();
d.getDay();
</pre>
In JavaScript, the first day of the week (0) means "Sunday", even if some countries in the world consider the first day of the week to be "Monday".
<br>
You can use an array of names, and <b>getDay()</b> to return the weekday as a name:
<pre>
const days = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"];
const d = new Date();
let day = days[d.getDay()];
</pre>
