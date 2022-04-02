<h1>width</h1>
If the <b>width</b> property is set to 100%, the video player will be responsive and scale up and down:
<pre>
video {
  width: 100%;
  height: auto;
}
</pre>
Notice that in the example above, the video player can be scaled up to be larger than its original size. A better solution, in many cases, will be to use the <b>max-width</b> property instead.
<h1>max-width</h1>
If the <b>max-width</b> property is set to 100%, the video player will scale down if it has to, but never scale up to be larger than its original size:
<pre>
video {
  max-width: 100%;
  height: auto;
}
</pre>
