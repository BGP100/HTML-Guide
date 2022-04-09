The <b>while</b> loop loops through a block of code as long as a specified condition is true.
<br>
<b>Syntax:</b>
<pre>
while (condition) {
  // code block to be executed
}
</pre>
In the following example, the code in the loop will run, over and over again, as long as a variable (i) is less than 10:
<pre>
while (i < 10) {
  text += "The number is " + i;
  i++;
}
</pre>
The <b>do while</b> loop is a variant of the while loop. This loop will execute the code block once, before checking if the condition is true, then it will repeat the loop as long as the condition is true.
<br>
<b>Syntax:</b>
<pre>
do {
  // code block to be executed
}
while (condition);
</pre>
The example below uses a <b>do while</b> loop. The loop will always be executed at least once, even if the condition is false, because the code block is executed before the condition is tested:
<pre>
do {
  text += "The number is " + i;
  i++;
}
while (i &lt; 10);
</pre>
Do not forget to increase the variable used in the condition, otherwise the loop will never end!
<h1>Comparing For and While</h1>
If you have read the previous chapter, about the for loop, you will discover that a while loop is much the same as a for loop, with statement 1 and statement 3 omitted.
<br>
The loop in this example uses a for loop to collect the car names from the cars array:
<pre>
const cars = ["BMW", "Volvo", "Saab", "Ford"];
let i = 0;
let text = "";
for (;cars[i];) {
  text += cars[i];
  i++;
}
</pre>
The loop in this example uses a while loop to collect the car names from the cars array:
<pre>
const cars = ["BMW", "Volvo", "Saab", "Ford"];
let i = 0;
let text = "";
while (cars[i]) {
  text += cars[i];
  i++;
}
</pre>
