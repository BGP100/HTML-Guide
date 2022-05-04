<a href="/JS/BOM/Timing.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="https://bledy-guides.repl.co/#bom">Next &gt;</a>
<hr>
Cookies let you store user information in web pages.
<h1>What are Them?</h1>
Cookies are data, stored in small text files, on your computer.
<br>
When a web server has sent a web page to a browser, the connection is shut down, and the server forgets everything about the user.
<br>
Cookies were invented to solve the problem "how to remember information about the user":
<ul>
  <li>When a user visits a web page, his/her name can be stored in a cookie.</li>
  <li>Next time the user visits the page, the cookie "remembers" his/her name.</li>
</ul>
Cookies are saved in name-value pairs like:
<pre>username = John Doe</pre>
When a browser requests a web page from a server, cookies belonging to the page are added to the request. This way the server gets the necessary data to "remember" information about users.
<br>
<b>IMPORTANT:</b> None of the examples below will work if your browser has local cookies support turned off.
<h1>Create a Cookie with JavaScript</h1>
JavaScript can create, read, and delete cookies with the <b>document.cookie</b> property.
<br>
With JavaScript, a cookie can be created like this:
<pre>document.cookie = "username=John Doe";</pre>
You can also add an expiry date (in UTC time). By default, the cookie is deleted when the browser is closed:
<pre>document.cookie = "username=John Doe; expires=Thu, 18 Dec 2013 12:00:00 UTC";</pre>
With a path parameter, you can tell the browser what path the cookie belongs to. By default, the cookie belongs to the current page.
<pre>document.cookie = "username=John Doe; expires=Thu, 18 Dec 2013 12:00:00 UTC; path=/";</pre>
<h1>Read a Cookie with JavaScript</h1>
With JavaScript, cookies can be read like this:
<pre>let x = document.cookie;</pre>
<h1>Change a Cookie with JavaScript</h1>
With JavaScript, you can change a cookie the same way as you create it:
<pre>document.cookie = "username=John Smith; expires=Thu, 18 Dec 2013 12:00:00 UTC; path=/";</pre>
The old cookie is overwritten.
<h1>Delete a Cookie with JavaScript</h1>
Deleting a cookie is very simple.
<br>
You don't have to specify a cookie value when you delete a cookie.
<br>
Just set the expires parameter to a past date:
<pre>document.cookie = "username=; expires=Thu, 01 Jan 1970 00:00:00 UTC; path=/;";</pre>
<h1>The Cookie String</h1>
The <b>document.cookie</b> property looks like a normal text string. But it is not.
<br>
Even if you write a whole cookie string to document.cookie, when you read it out again, you can only see the name-value pair of it.
<br>
If you set a new cookie, older cookies are not overwritten. The new cookie is added to document.cookie, so if you read document.cookie again you will get something like:
<br>
<code>cookie1 = value; cookie2 = value;</code>
<br>
If you want to find the value of one specified cookie, you must write a JavaScript function that searches for the cookie value in the cookie string.
<h1>Example</h1>
In the example to follow, we will create a cookie that stores the name of a visitor.
<br>
The first time a visitor arrives to the web page, he/she will be asked to fill in his/her name. The name is then stored in a cookie.
<br>
The next time the visitor arrives at the same page, he/she will get a welcome message.
<br>
For the example we will create 3 JavaScript functions:
<ol>
  <li>A function to set a cookie value</li>
  <li>A function to get a cookie value</li>
  <li>A function to check a cookie value</li>
</ol>
<h1>A Function to Set a Cookie</h1>
First, we create a <b>function</b> that stores the name of the visitor in a cookie variable:
<pre>
function setCookie(cname, cvalue, exdays) {
  const d = new Date();
  d.setTime(d.getTime() + (exdays*24*60*60*1000));
  let expires = "expires="+ d.toUTCString();
  document.cookie = cname + "=" + cvalue + ";" + expires + ";path=/";
}
</pre>
<b>Explained:</b>
<br>
The parameters of the function above are the name of the cookie (cname), the value of the cookie (cvalue), and the number of days until the cookie should expire (exdays).
<br>
The function sets a cookie by adding together the cookiename, the cookie value, and the expires string.
<h1>A Function to Get a Cookie</h1>
Then, we create a <b>function</b> that returns the value of a specified cookie:
<pre>
function getCookie(cname) {
  let name = cname + "=";
  let decodedCookie = decodeURIComponent(document.cookie);
  let ca = decodedCookie.split(';');
  for(let i = 0; i &lt; ca.length; i++) {
    let c = ca[i];
    while (c.charAt(0) == ' ') {
      c = c.substring(1);
    }
    if (c.indexOf(name) == 0) {
      return c.substring(name.length, c.length);
    }
  }
  return "";
}
</pre>
<b>Explained:</b>
<br>
Take the cookiename as parameter (cname).
<br>
Create a variable (name) with the text to search for (cname + "=").
<br>
Decode the cookie string, to handle cookies with special characters, e.g. '$'
<br>
Split document.cookie on semicolons into an array called ca (ca = decodedCookie.split(';')).
<br>
Loop through the ca array (i = 0; i < ca.length; i++), and read out each value c = ca[i]).
<br>
If the cookie is found (c.indexOf(name) == 0), return the value of the cookie (c.substring(name.length, c.length).
<br>
If the cookie is not found, return "".
<h1>A Function to Check a Cookie</h1>
Last, we create the function that checks if a cookie is set.
<br>
If the cookie is set it will display a greeting.
<br>
If the cookie is not set, it will display a prompt box, asking for the name of the user, and stores the username cookie for 365 days, by calling the setCookie function:
<pre>
function checkCookie() {
  let username = getCookie("username");
  if (username != "") {
   alert("Welcome again " + username);
  } else {
    username = prompt("Please enter your name:", "");
    if (username != "" && username != null) {
      setCookie("username", username, 365);
    }
  }
}
</pre>
<h1>All Code Together Now</h1>
<pre>
function setCookie(cname, cvalue, exdays) {
  const d = new Date();
  d.setTime(d.getTime() + (exdays * 24 * 60 * 60 * 1000));
  let expires = "expires=" + d.toUTCString();
  document.cookie = cname + "=" + cvalue + ";" + expires + ";path=/";
}
function getCookie(cname) {
  let name = cname + "=";
  let ca = document.cookie.split(';');
  for(let i = 0; i &lt; ca.length; i++) {
    let c = ca[i];
    while (c.charAt(0) == ' ') {
      c = c.substring(1);
    }
    if (c.indexOf(name) == 0) {
      return c.substring(name.length, c.length);
    }
  }
  return "";
}
function checkCookie() {
  let user = getCookie("username");
  if (user != "") {
    alert("Welcome again " + user);
  } else {
    user = prompt("Please enter your name:", "");
    if (user != "" && user != null) {
      setCookie("username", user, 365);
    }
  }
}
</pre>
The example above runs the <b>checkCookie()</b> function when the page loads.
