<h1>What is it?</h1>
The viewport is the user's visible area of a web page.
<br>
The viewport varies with the device, and will be smaller on a mobile phone than on a computer screen.
<br>
Before tablets and mobile phones, web pages were designed only for computer screens, and it was common for web pages to have a static design and a fixed size.
<br>
Then, when we started surfing the internet using tablets and mobile phones, fixed size web pages were too large to fit the viewport. To fix this, browsers on those devices scaled down the entire web page to fit the screen.
<br>
This was not perfect!! But a quick fix.
<h1>Setting the Viewport</h1>
To create a responsive website, add the following <b>&lt;meta&gt;</b> tag to all your web pages:
<pre>&lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;</pre>
This will set the viewport of your page, which will give the browser instructions on how to control the page's dimensions and scaling.
<br>
Here is an example of a web page without the viewport meta tag, and the same web page with the viewport meta tag:
<p></p>
<b>Without viewport:</b>
<img src="https://i.imgur.com/a3YL2Oy.png">
<p></p>
<b>With viewport:</b>
<img src="https://i.imgur.com/kpxDfHy.png">
<h1>Images</h1>
Responsive images are images that scale nicely to fit any browser size.
<h2>width</h2>
If the CSS <b>width</b> property is set to 100%, the image will be responsive and scale up and down:
<br>
<img src="https://i.imgur.com/EZqJ6si.jpg" width="100%">
<pre>&lt;img src="img_girl.jpg" style="width:100%;"&gt;</pre>
Notice that in the example above, the image can be scaled up to be larger than its original size. A better solution, in many cases, will be to use the max-width property instead.
<h1>Size Content to Viewport</h1>
Users are used to scroll websites vertically on both desktop and mobile devices - but not horizontally!
<br>
So, if the user is forced to scroll horizontally, or zoom out, to see the whole web page it results in a poor user experience.
<br>
Some additional rules to follow:
<br>
<b>1. Do NOT use large fixed width elements</b> - For example, if an image is displayed at a width wider than the viewport it can cause the viewport to scroll horizontally. Remember to adjust this content to fit within the width of the viewport.
<br>
<b>2. Do NOT let the content rely on a particular viewport width to render well</b> - Since screen dimensions and width in CSS pixels vary widely between devices, content should not rely on a particular viewport width to render well.
<br>
<b>3. Use CSS media queries to apply different styling for small and large screens</b> - Setting large absolute CSS widths for page elements will cause the element to be too wide for the viewport on a smaller device. Instead, consider using relative width values, such as width: 100%. Also, be careful of using large absolute positioning values. It may cause the element to fall outside the viewport on small devices.
