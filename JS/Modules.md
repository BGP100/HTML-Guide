<a href="/JS/Arrows.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Debugging.md">Next &gt;</a>
<hr>
JavaScript modules allow you to break up your code into separate files.
<br>
This makes it easier to maintain the code-base.
<br>
JavaScript modules rely on the <b>import</b> and <b>export</b> statements.
<h1>Export</h1>
You can export a function or variable from any file.
<br>
Let us create a file named <b>person.js</b>, and fill it with the things we want to export.
<br>
There are two types of exports: Named and Default.
<h1>Named Exports</h1>
You can create named exports two ways. In-line individually, or all at once at the bottom.
<br>
In-line individually:
<pre>
export const name = "Jesse";
export const age = 40;
</pre>
All at once at the bottom:
<pre>
const name = "Jesse";
const age = 40;
export {name, age};
</pre>
<h1>Default Exports</h1>
Let us create another file, named <b>message.js</b>, and use it for demonstrating default export.
<br>
You can only have one default export in a file.
<pre>
const message = () => {
const name = "Jesse";
const age = 40;
return name + ' is ' + age + 'years old.';
};
export default message;
</pre>
<h1>Import</h1>
You can import modules into a file in two ways, based on if they are named exports or default exports.
<br>
Named exports are constructed using curly braces. Default exports are not.
<pre>import {name, age} from "./person.js";</pre>
<pre>import message from "./message.js";</pre>
<h1>Note</h1>
Modules only work with the HTTP(s) protocol.
<br>
A web-page opened via the <code>file://</code> protocol cannot use import / export.
