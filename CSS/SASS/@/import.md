Sass keeps the CSS code DRY (Don't Repeat Yourself). One way to write DRY code is to keep related code in separate files.
<br>
You can create small files with CSS snippets to include in other Sass files. Examples of such files can be: reset file, variables, colors, fonts, font-sizes, etc.
<h1>Importing Files</h1>
Just like CSS, Sass also supports the <b>@import</b> directive.
<br>
The <b>@import</b> directive allows you to include the content of one file in another.
<br>
The CSS <b>@import</b> directive has a major drawback due to performance issues; it creates an extra HTTP request each time you call it. However, the Sass <b>@import</b> directive includes the file in the CSS; so no extra HTTP call is required at runtime!
<pre>@import <i>filename</i>;</pre>
<b>Tip:</b> You do not need to specify a file extension, Sass automatically assumes that you mean a .sass or .scss file. You can also import CSS files. The @import directive imports the file and any variables or mixins defined in the imported file can then be used in the main file.
<br>
You can import as many files as you need in the main file:
<pre>
@import "variables";
@import "colors";
@import "reset";
</pre>
Let's look at an example: Let's assume we have a reset file called "reset.scss", that looks like this:
<pre>
html, body, ul, ol {
  margin: 0;
  padding: 0;
}
</pre>
and now we want to import the "reset.scss" file into another file called "standard.scss".
<br>
Here is how we do it: It is normal to add the @import directive at the top of a file; this way its content will have a global scope:
<pre>
@import "reset";
body {
  font-family: Helvetica, sans-serif;
  font-size: 18px;
  color: red;
}
</pre>
So, when the "standard.css" file is transpiled, the CSS will look like this:
<pre>
html, body, ul, ol {
  margin: 0;
  padding: 0;
}
body {
  font-family: Helvetica, sans-serif;
  font-size: 18px;
  color: red;
}
</pre>
<h1>Partials</h1>
By default, Sass transpiles all the .scss files directly. However, when you want to import a file, you do not need the file to be transpiled directly.
<br>
Sass has a mechanism for this: If you start the filename with an underscore, Sass will not transpile it. Files named this way are called partials in Sass.
<br>
So, a partial Sass file is named with a leading underscore:
<pre>_<i>filename</i>;</pre>
The following example shows a partial Sass file named <code>_colors.scss</code>. (This file will not be transpiled directly to "colors.css"):
<pre>
$myPink: #EE82EE;
$myBlue: #4169E1;
$myGreen: #8FBC8F;
</pre>
Now, if you import the partial file, omit the underscore. Sass understands that it should import the file <code>_colors.scss</code>:
<pre>
@import "colors";
body {
  font-family: Helvetica, sans-serif;
  font-size: 18px;
  color: $myBlue;
}
</pre>
