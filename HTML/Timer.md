In here you will learn how to do a countdown in HTML just like the example below:
<br>
<img src="https://i.imgur.com/XJo7EHk.png">
<h1>CSS</h1>
<pre>
body {
  text-align: center;
  background-color: #ffffff;
}
</pre>
<h1>HTML</h1>
<pre>&lt;h2 color="#333"&gt;Timer until 9999&lt;/h2&gt;</pre>
<h1>JavaScript</h1>
<pre>
/* Set the date we're counting down to */
var countDownDate = new Date("Jan 1, 9999 00:00:00").getTime();
/* Update the count down every 1 second */
var x = setInterval(function() {
/* Get today's date and time */
var now = new Date().getTime();
/* Find the distance between now and the count down date */
var distance = countDownDate - now;
/* Time calculations for days, hours, minutes and seconds */
var days = Math.floor(distance / (1000 * 60 * 60 * 24));
var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
var seconds = Math.floor((distance % (1000 * 60)) / 1000);
/* Display the result in the element with id="demo" */
document.getElementById("demo").innerHTML = days + "d " + hours + "h "
+ minutes + "m " + seconds + "s ";
/* If the count down is finished, write some text */
if (distance < 0) {
  clearInterval(x);
  document.getElementById("demo").innerHTML = "Countdown has ended, wait until update.";
  }
}, 1000);
</pre>
