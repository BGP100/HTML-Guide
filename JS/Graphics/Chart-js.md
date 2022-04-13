<a href="/JS/Graphics/Plotly-js.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Graphics/Google-Chart.md">Next &gt;</a>
<hr>
Chart.js comes with the following built-in chart types:
<ul>
  <li>Scatter</li>
  <li>Line</li>
  <li>Bar</li>
  <li>Radar</li>
  <li>Pie and Doughnut</li>
  <li>Polar Area</li>
  <li>Bubble</li>
</ul>
<h1>How To Use it?</h1>
Chart.js is easy to use.
<br>
First, add a link to the providing CDN (Content Delivery Network):
<pre>script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.9.4/Chart.js"&gt;&lt;/script&gt;</pre>
Then, add a <b>&lt;canvas&gt;</b> to where you want to draw the chart:
<pre>canvas id="myChart" style="width:100%;max-width:700px"&gt;&lt;/canvas&gt;</pre>
The canvas element must have a unique id.
<br>
That's all!
<br>
Typical Scatter Chart Syntax:
<pre>
var myChart = new Chart("myChart", {
  type: "scatter",
  data: {},
  options: {}
});
</pre>
Typical Line Chart Syntax:
<pre>
var myChart = new Chart("myChart", {
  type: "line",
  data: {},
  options: {}
});
</pre>
Typical Bar Chart Syntax:
<pre>
var myChart = new Chart("myChart", {
  type: "bar",
  data: {},
  options: {}
});
</pre>
<h1>Scatter Graphs</h1>
<img src="https://i.imgur.com/ToK7WwH.jpg" width="69%">
<pre>
var xyValues = [
  {x:50, y:7},
  {x:60, y:8},
  {x:70, y:8},
  {x:80, y:9},
  {x:90, y:9},
  {x:100, y:9},
  {x:110, y:10},
  {x:120, y:11},
  {x:130, y:14},
  {x:140, y:14},
  {x:150, y:15}
];
new Chart("myChart", {
  type: "scatter",
  data: {
    datasets: [{
      pointRadius: 4,
      pointBackgroundColor: "rgba(0,0,255,1)",
      data: xyValues
    }]
  },
  options:{...}
});
</pre>
<h1>Line Graphs</h1>
<img src="https://i.imgur.com/91UzGq5.jpg" width="69%">
<pre>
var xValues = [50,60,70,80,90,100,110,120,130,140,150];
var yValues = [7,8,8,9,9,9,10,11,14,14,15];
new Chart("myChart", {
  type: "line",
  data: {
    labels: xValues,
    datasets: [{
      backgroundColor: "rgba(0,0,0,1.0)",
      borderColor: "rgba(0,0,0,0.1)",
      data: yValues
    }]
  },
  options:{...}
});
</pre>
If you set the borderColor to zero, you can scatter plot the line graph:
<pre>borderColor: "rgba(0,0,0,0)",</pre>
<h1>Multiline Graphs</h1>
<img src="https://i.imgur.com/wJLxP2y.jpg" width="69%">
<pre>
var xValues = [100,200,300,400,500,600,700,800,900,1000];
new Chart("myChart", {
  type: "line",
  data: {
    labels: xValues,
    datasets: [{
      data: [860,1140,1060,1060,1070,1110,1330,2210,7830,2478],
      borderColor: "red",
      fill: false
    },{
      data: [1600,1700,1700,1900,2000,2700,4000,5000,6000,7000],
      borderColor: "green",
      fill: false
    },{
      data: [300,700,2000,5000,6000,4000,2000,1000,200,100],
      borderColor: "blue",
      fill: false
    }]
  },
  options: {
    legend: {display: false}
  }
});
</pre>
<h1>Linear Graphs</h1>
<img src="https://i.imgur.com/cdqizOK.jpg" width="69%">
<pre>
var xValues = [];
var yValues = [];
generateData("x * 2 + 7", 0, 10, 0.5);
new Chart("myChart", {
  type: "line",
  data: {
    labels: xValues,
    datasets: [{
      fill: false,
      pointRadius: 1,
      borderColor: "rgba(255,0,0,0.5)",
      data: yValues
    }]
  },
  options: {...}
});
function generateData(value, i1, i2, step = 1) {
  for (let x = i1; x <= i2; x += step) {
    yValues.push(eval(value));
    xValues.push(x);
  }
}
</pre>
<h1>Function Graphs</h1>
<img src="https://i.imgur.com/UTWQKi6.jpg" width="69%">
<pre>generateData("Math.sin(x)", 0, 10, 0.5);</pre>
<h1>Bar Graphs</h1>
<img src="https://i.imgur.com/KgbDhgk.jpg" width="69%">
<pre>
var xValues = ["Italy", "France", "Spain", "USA", "Argentina"];
var yValues = [55, 49, 44, 24, 15];
var barColors = ["red", "green","blue","orange","brown"];
new Chart("myChart", {
  type: "bar",
  data: {
    labels: xValues,
    datasets: [{
      backgroundColor: barColors,
      data: yValues
    }]
  },
  options: {...}
});
</pre>
Color only one bar:
<pre>var barColors = ["blue"];</pre>
Same color all bars:
<pre>var barColors = "red";</pre>
Color Shades:
<pre>
var barColors = [
  "rgba(0,0,255,1.0)",
  "rgba(0,0,255,0.8)",
  "rgba(0,0,255,0.6)",
  "rgba(0,0,255,0.4)",
  "rgba(0,0,255,0.2)",
];
</pre>
Just change type from "bar" to "horizontalBar":
<pre>type: "horizontalBar",</pre>
<h1>Pie Graphs</h1>
<img src="https://i.imgur.com/KxmdHJo.jpg" width="69%">
<pre>
new Chart("myChart", {
  type: "pie",
  data: {
    labels: xValues,
    datasets: [{
      backgroundColor: barColors,
      data: yValues
    }]
  },
  options: {
    title: {
      display: true,
      text: "World Wide Wine Production"
    }
  }
});
</pre>
<h1>Doughnut Graphs</h1>
<img src="https://i.imgur.com/B9264FP.jpg" width="69%">
<br>
Just change type from "pie" to "doughnut":
<pre>type: "doughnut";</pre>
