<a href="/JS/Arrays/Const.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Date/Formats.md">Next &gt;</a>
<hr>
JavaScript Date Object lets us work with dates.
<pre>const d = new Date();</pre>
<h1>Creating Dates</h1>
Date objects are created with the new Date() constructor.
<br>
There are 4 ways to create a new date object:
<pre>
new Date()
new Date(year, month, day, hours, minutes, seconds, milliseconds)
new Date(milliseconds)
new Date(date string)
</pre>
<h1>new Date()</h1>
<b>new Date()</b> creates a new date object with the current date and time:
<pre>const d = new Date();</pre>
<h2>new Date(year, month, ...)</h2>
<b>new Date(year, month, ...)</b> creates a new date object with a specified date and time.
<br>
7 numbers specify year, month, day, hour, minute, second, and millisecond (in that order):
<pre>const d = new Date(2018, 11, 24, 10, 33, 30, 0);</pre>
<b>Note:</b> JavaScript counts months from 0 to 11:
<b>
January = 0.
</b>
December = 11.
<p></p>
Specifying a month higher than 11, will not result in an error but add the overflow to the next year:
<pre>const d = new Date(2018, 15, 24, 10, 33, 30);</pre>
Is the same as:
<pre>const d = new Date(2019, 3, 24, 10, 33, 30);</pre>
Specifying a day higher than max, will not result in an error but add the overflow to the next month:
<pre>const d = new Date(2018, 5, 35, 10, 33, 30);</pre>
Is the same as:
<pre>const d = new Date(2018, 6, 5, 10, 33, 30);</pre>
<h2>new Date(dateString)</h2>
<b>new Date(dateString)</b> creates a new date object from a date string:
<pre>const d = new Date("October 13, 2014 11:13:00");</pre>
<h2>new Date(milliseconds)</h2>
new Date(milliseconds) creates a new date object as zero time plus milliseconds:
<pre>const d = new Date(0);</pre>
01 January 1970 plus 100 000 000 000 milliseconds is approximately 03 March 1973:
<pre>const d = new Date("tel:100000000000"&gt;100000000000);</pre>
January 01 1970 minus 100 000 000 000 milliseconds is approximately October 31 1966:
<pre>const d = new Date(-100000000000);</pre>
<pre>const d = new Date(86400000);</pre>
<h1>Using Numbers</h1>
6 numbers specify year, month, day, hour, minute, second:
<pre>const d = new Date(2018, 11, 24, 10, 33, 30);</pre>
5 numbers specify year, month, day, hour, and minute:
<pre>const d = new Date(2018, 11, 24, 10, 33);</pre>
4 numbers specify year, month, day, and hour:
<pre>const d = new Date(2018, 11, 24, 10);</pre>
3 numbers specify year, month, and day:
<pre>const d = new Date(2018, 11, 24);</pre>
2 numbers specify year and month:
<pre>const d = new Date(2018, 11);</pre>
<h1>Previous Century</h1>
One and two digit years will be interpreted as 19xx:
<pre>const d = new Date(99, 11, 24);</pre>
<pre>const d = new Date(9, 11, 24);</pre>
<h1>Methods</h1>
When a Date object is created, a number of methods allow you to operate on it.
<br>
Date methods allow you to get and set the year, month, day, hour, minute, second, and millisecond of date objects, using either local time or UTC (universal, or GMT) time.
<h1>Displaying Dates</h1>
JavaScript will (by default) output dates in full text string format:
<br>
<code>Thu Apr 07 2022 11:09:00 GMT-0500 (CDT)</code>
<p></p>
When you display a date object in HTML, it is automatically converted to a string, with the <b>toString()</b> method.
<pre>
const d = new Date();
d.toString();
</pre>
The <b>toUTCString()</b> method converts a date to a UTC string (a date display standard).
<pre>
const d = new Date();
d.toUTCString();
</pre>
The <b>toDateString()</b> method converts a date to a more readable format:
<pre>
const d = new Date();
d.toDateString();
</pre>
The <b>toISOString()</b> method converts a Date object to a string, using the ISO standard format:
</pre>
const d = new Date();
d.toISOString();
</pre>
