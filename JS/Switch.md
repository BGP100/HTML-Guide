The <b>switch</b> statement is used to perform different actions based on different conditions.
<hr>
<b>Syntax:</b>
<pre>
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
</pre>
This is how it works:
<ul>
  <li>The switch expression is evaluated once.</li>
  <li>The value of the expression is compared with the values of each case.</li>
  <li>If there is a match, the associated block of code is executed.</li>
  <li>If there is no match, the default code block is executed.</li>
</ul>
The getDay() method returns the weekday as a number between 0 and 6.
<br>
<b>(Sunday=0, Monday=1, Tuesday=2 ..)</b>
<br>
This example uses the weekday number to calculate the weekday name:
<pre>
switch (new Date().getDay()) {
  case 0:
    day = "Sunday";
    break;
  case 1:
    day = "Monday";
    break;
  case 2:
     day = "Tuesday";
    break;
  case 3:
    day = "Wednesday";
    break;
  case 4:
    day = "Thursday";
    break;
  case 5:
    day = "Friday";
    break;
  case 6:
    day = "Saturday";
}
</pre>
<h1>break</h1>
When JavaScript reaches a <b>break</b> keyword, it breaks out of the switch block.
<br>
This will stop the execution inside the switch block.
<br>
It is not necessary to break the last case in a switch block. The block breaks (ends) there anyway.
<h1>default</h1>
The <b>default</b> keyword specifies the code to run if there is no case match:
<pre>
switch (new Date().getDay()) {
  case 6:
    text = "Today is Saturday";
    break;
  case 0:
    text = "Today is Sunday";
    break;
  default:
    text = "Looking forward to the Weekend";
}
</pre>
The <b>default</b> case does not have to be the last case in a switch block:
<pre>
switch (new Date().getDay()) {
  default:
    text = "Looking forward to the Weekend";
    break;
  case 6:
    text = "Today is Saturday";
    break;
  case 0:
    text = "Today is Sunday";
}
</pre>
<h1>Common Code Blocks</h1>
Sometimes you will want different switch cases to use the same code.
<br>
In this example case 4 and 5 share the same code block, and 0 and 6 share another code block:
<pre>
switch (new Date().getDay()) {
  case 4:
  case 5:
    text = "Soon it is Weekend";
    break;
  case 0:
  case 6:
    text = "It is Weekend";
    break;
  default:
    text = "Looking forward to the Weekend";
}
</pre>
<h1>Switching Details</h1>
If multiple cases matches a case value, the first case is selected.
<br>
If no matching cases are found, the program continues to the default label.
<br>
If no default label is found, the program continues to the statement(s) after the switch.
<h1>Strict Comparison</h1>
Switch cases use strict comparison (<code>===</code>).
<br>
The values must be of the same type to match.
<br>
A strict comparison can only be true if the operands are of the same type.
<br>
In this example there will be no match for x:
<pre>
let x = "0";
switch (x) {
  case 0:
    text = "Off";
    break;
  case 1:
    text = "On";
    break;
  default:
    text = "No value found";
}
</pre>
