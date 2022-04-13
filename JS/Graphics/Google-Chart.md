<a href="/JS/Graphics/Chart-js.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Graphics/D3-js.md">Next &gt;</a>
<hr>
From simple line charts to complex hierarchical tree maps, the Google Chart gallery provides a large number of ready-to-use chart types:
<ul>
  <li>Scatter Chart</li>
  <li>Line Chart</li>
  <li>Bar / Column Chart</li>
  <li>Area Chart</li>
  <li>Pie Chart</li>
  <li>Donut Chart</li>
  <li>Org Chart</li>
  <li>Map / Geo Chart</li>
</ul>
<h1>How To Use it?</h1>
To use Google Chart in your web page, add a link to the charts loader:
<pre>&lt;script src="https://www.gstatic.com/charts/loader.js"&gt;&lt;/script&gt;</pre>
Google Chart is easy to use.
<br>
Just add a <b>&lt;div&gt;</b> element to display the chart:
<pre>&lt;div id="myChart" style="max-width:700px; height:400px"&gt;&lt;/div&gt;</pre>
The <b>&lt;div&gt;</b> element must have a unique id.
<br>
Then load the Google Graph API:
<ol>
  <li>Load the Visualization API and the corechart package</li>
  <li>Set a callback function to call when the API is loaded</li>
</ol>
<pre>
1 google.charts.load('current',{packages:['corechart']});
2 google.charts.setOnLoadCallback(drawChart);
</pre>
<h1>Line Graphs</h1>
<img src="https://i.imgur.com/BxnE492.png" width="69%">
<pre>
function drawChart() {
// Set Data
var data = google.visualization.arrayToDataTable([
  ['Price', 'Size'],
  [50,7],[60,8],[70,8],[80,9],[90,9],[100,9],
  [110,10],[120,11],[130,14],[140,14],[150,15]
  ]);
// Set Options
var options = {
  title: 'House Prices vs Size',
  hAxis: {title: 'Square Meters'},
  vAxis: {title: 'Price in Millions'},
  legend: 'none'
};
// Draw Chart
var chart = new google.visualization.LineChart(document.getElementById('myChart'));
chart.draw(data, options);
}
</pre>
<h1>Scatter Graphs</h1>
<img src="https://i.imgur.com/V3YILiZ.png" width="69%">
<pre>var chart = new google.visualization.ScatterChart(document.getElementById('myChart'));</pre>
<h1>Bar Graphs</h1>
<img src="https://i.imgur.com/oY92N5R.png" width="69%">
<pre>
function drawChart() {
var data = google.visualization.arrayToDataTable([
  ['Contry', 'Mhl'],
  ['Italy', 55],
  ['France', 49],
  ['Spain', 44],
  ['USA', 24],
  ['Argentina', 15]
]);
var options = {
  title: 'World Wide Wine Production'
};
var chart = new google.visualization.BarChart(document.getElementById('myChart'));
chart.draw(data, options);
}
</pre>
<h1>Pie Graphs</h1>
<img src="https://i.imgur.com/07FgGoZ.png" width="69%">
<pre>var chart = new google.visualization.PieChart(document.getElementById('myChart'));</pre>
<h1>3D Pie Graphs</h1>
<img src="https://i.imgur.com/hMqD7Ro.png" width="69%">
<pre>
var options = {
  title: 'World Wide Wine Production',
  <b>is3D: true</b>
};
</pre>
