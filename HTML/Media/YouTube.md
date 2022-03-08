The easiest way to play videos in HTML, is through YouTube.
<h1>Struggling with Video Formats?</h1>
Converting videos to different formats can be difficult and time-consuming.
<br>
An easier solution is to let YouTube play the videos in your web page.
<h1>YT Video id</h1>
YouTube will display an id (like tgbNymZ7vqY), when you save (or play) a video.
<br>
You can use this id, and refer to your video in the HTML code.
<h1>Playing a YT Video in HTML</h1>
To play your video on a web page, do the following:
<ul>
  <li>Upload the video to YouTube.</li>
  <li>Take a note of the video id.</li>
  <li>Define an &lt;iframe&lt; element in your web page.</li>
  <li>Let the src attribute point to the video URL.</li>
  <li>Use the width and height attributes to specify the dimension of the player.</li>
  <li>Add any other parameters to the URL (see below).</li>
</ul>
<pre>&lt;iframe width="420" height="315" src="//www.youtube.com/embed/tgbNymZ7vqY"&gt;&lt;/iframe&gt;</pre>
<h1>autoplay + mute</h1>
You can let your video start playing automatically when a user visits the page, by adding autoplay=1 to the YouTube URL. However, automatically starting a video is annoying for your visitors!
<br>
Add mute=1 after autoplay=1 to let your video start playing automatically but muted.
<pre>&lt;iframe width="420" height="315" src="//www.youtube.com/embed/tgbNymZ7vqY?autoplay=1&mute=1"&gt;&lt;/iframe&gt;</pre>
<h1>Playlists</h1>
A comma separated list of videos to play (in addition to the original URL).
<h1>Loops</h1>
Add loop=1 to let your video loop forever.
<br>
Value 0 (default): The video will play only once.
<br>
Value 1: The video will loop (forever).
<pre>&lt;iframe width="420" height="315" src="//www.youtube.com/embed/tgbNymZ7vqY?playlist=tgbNymZ7vqY&loop=1"&gt;&lt;/iframe&gt;</pre>
<h1>Controls</h1>
Add controls=0 to not display controls in the video player.
<br>
Value 0: Player controls does not display.
<br>
Value 1 (default): Player controls display.
<pre>&lt;iframe width="420" height="315" src="//www.youtube.com/embed/tgbNymZ7vqY?controls=0"&gt;&lt;/iframe&gt;</pre>
<pre>&lt;iframe width="420" height="315" src="//www.youtube.com/embed/tgbNymZ7vqY?controls=1"&gt;&lt;/iframe&gt;</pre>
