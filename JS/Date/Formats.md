<h1>Output</h1>
Independent of input format, JavaScript will (by default) output dates in full text string format:
<p></p>
<code>Sat Apr 09 2022 10:18:27 GMT-0500 (hora de verano central)</code>
<h1>ISO Dates</h1>
ISO 8601 is the international standard for the representation of dates and times.
<br>
The ISO 8601 syntax (YYYY-MM-DD) is also the preferred JavaScript date format:
<pre>const d = new Date("2015-03-25");</pre>
<b>Note:</b> The computed date will be relative to your time zone. Depending on your time zone, the result above will vary between March 24 and March 25.
<h2>Year and Month</h2>
ISO dates can be written without specifying the day (YYYY-MM):
<pre>const d = new Date("2015-03");</pre>
<h2>Only Year</h2>
ISO dates can be written without month and day (YYYY):
<pre>const d = new Date("2015");</pre>
<h2>Date-Time</h2>
ISO dates can be written with added hours, minutes, and seconds (YYYY-MM-DDTHH:MM:SSZ):
pre>const d = new Date("2015-03-25T12:00:00Z");</pre>
Date and time is separated with a capital T.
<br>
UTC time is defined with a capital letter Z.
<br>
If you want to modify the time relative to UTC, remove the Z and add +HH:MM or -HH:MM instead:
<pre>const d = new Date("2015-03-25T12:00:00-06:30");</pre>
<h1>Time Zones</h1>
When setting a date, without specifying the time zone, JavaScript will use the browser's time zone.
<br>
When getting a date, without specifying the time zone, the result is converted to the browser's time zone.
<br>
In other words: If a date/time is created in GMT (Greenwich Mean Time), the date/time will be converted to CDT (Central US Daylight Time) if a user browses from central US.
<h1>Short Dates</h1>
Short dates are written with an "MM/DD/YYYY" syntax like this:
<pre>const d = new Date("03/25/2015");</pre>
<h1>WARNINGS!!</h1>
In some browsers, months or days with no leading zeroes may produce an error:
<pre>const d = new Date("2015-3-25");</pre>
The behavior of "YYYY/MM/DD" is undefined.
<br>
Some browsers will try to guess the format. Some will return NaN.
<pre>const d = new Date("2015/03/25");</pre>
The behavior of  "DD-MM-YYYY" is also undefined.
<br>
Some browsers will try to guess the format. Some will return NaN.
<pre>const d = new Date("25-03-2015");</pre>
<h1>Long Dates</h1>
Long dates are most often written with a "MMM DD YYYY" syntax like this:
<pre>const d = new Date("Mar 25 2015");</pre>
Month and day can be in any order:
<pre>const d = new Date("25 Mar 2015");</pre>
And, month can be written in full (January), or abbreviated (Jan):
<pre>const d = new Date("January 25 2015");</pre>
<pre>const d = new Date("Jan 25 2015");</pre>
Commas are ignored. Names are case insensitive:
<pre>const d = new Date("JANUARY, 25, 2015");</pre>
<h1>Parsing Dates</h1>
If you have a valid date string, you can use the Date.parse() method to convert it to milliseconds.
<br>
<b>Date.parse()</b> returns the number of milliseconds between the date and January 1, 1970:
<pre>let msec = Date.parse("March 21, 2012");</pre>
You can then use the number of milliseconds to convert it to a date object:
<pre>
let msec = Date.parse("March 21, 2012");
const d = new Date(msec);
</pre>
