<a href="/JS/Graphics/Main.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Graphics/Chart-js.md">Next &gt;</a>
<hr>
Plotly.js is a charting library that comes with over 40 chart types, 3D charts, statistical graphs, and SVG maps.
<h1>Scatter Graphs</h1>
<img src="https://i.imgur.com/SI30tRa.jpg" width="69%">
<pre>
var xArray = [50,60,70,80,90,100,110,120,130,140,150];
var yArray = [7,8,8,9,9,9,10,11,14,14,15];
// Define Data
var data = [{
  x: xArray,
  y: yArray,
  mode:"markers",
  type:"scatter"
}];
// Define Layout
var layout = {
  xaxis: {range: [40, 160], title: "Square Meters"},
  yaxis: {range: [5, 16], title: "Price in Millions"},
  title: "House Prices vs. Size"
};
Plotly.newPlot("myPlot", data, layout);
</pre>
<h1>Line Graphs</h1>
<img src="https://i.imgur.com/BxnE492.jpg" width="69%">
<pre>
var xArray = [50,60,70,80,90,100,110,120,130,140,150];
var yArray = [7,8,8,9,9,9,10,11,14,14,15];
// Define Data
var data = [{
  x: xArray,
  y: yArray,
  mode: "lines",
  type: "scatter"
}];
// Define Layout
var layout = {
  xaxis: {range: [40, 160], title: "Square Meters"},
  yaxis: {range: [5, 16], title: "Price in Millions"},
  title: "House Prices vs Size"
};
// Display using Plotly
Plotly.newPlot("myPlot", data, layout);
</pre>
<h1>Linear Graphs</h1>
<img src="https://i.imgur.com/NbMmCWY.png" width="69%">
<pre>
var exp = "x + 17";
// Generate values
var xValues = [];
var yValues = [];
for (var x = 0; x <= 10; x += 1) {
  yValues.push(eval(exp));
  xValues.push(x);
}
// Define Data
var data = [{
  x: xValues,
  y: yValues,
  mode: "lines"
}];
// Define Layout
var layout = {title: "y = " + exp};
// Display using Plotly
Plotly.newPlot("myPlot", data, layout);
</pre>
<h1>Multiline Graphs</h1>
<img src="https://i.imgur.com/YV20WmX.png" width="69%">
<pre>
var exp1 = "x";
var exp2 = "1.5*x";
var exp3 = "1.5*x + 7";
// Generate values
var x1Values = [];
var x2Values = [];
var x3Values = [];
var y1Values = [];
var y2Values = [];
var y3Values = [];
for (var x = 0; x <= 10; x += 1) {
  x1Values.push(x);
  x2Values.push(x);
  x3Values.push(x);
  y1Values.push(eval(exp1));
  y2Values.push(eval(exp2));
  y3Values.push(eval(exp3));
}
// Define Data
var data = [
  {x: x1Values, y: y1Values, mode:"lines"},
  {x: x2Values, y: y2Values, mode:"lines"},
  {x: x3Values, y: y3Values, mode:"lines"}
];
// Define Layout
var layout = {title: "[y=" + exp1 + "] [y=" + exp2 + "] [y=" + exp3 + "]"};
// Display using Plotly
Plotly.newPlot("myPlot", data, layout);
</pre>
<h1>Bar Graphs</h1>
<img src="https://i.imgur.com/n4yD02E.png" width="69%">
<pre>
var xArray = ["Italy","France","Spain","USA","Argentina"];
var yArray = [55, 49, 44, 24, 15];
var data = [{
  x: xArray,
  y: yArray,
  type: "bar"  }];
var layout = {title:"World Wine Wine Production"};
Plotly.newPlot("myPlot", data, layout);
</pre>
<h1>Horizontal Bar Graphs</h1>
<img src="https://i.imgur.com/NggqzJC.png" width="69%">
<pre>
var xArray = [55, 49, 44, 24, 15];
var yArray = ["Italy","France","Spain","USA","Argentina"];
var data = [{
  x: xArray,
  y: yArray,
  type: "bar",
  orientation: "h"
}];
var layout = {title:"World Wine Wine Production"};
Plotly.newPlot("myPlot", data, layout);
</pre>
<h1>Pie Graphs</h1>
<img src="https://i.imgur.com/sUU4B9f.png" width="69%">
<pre>
var data = [{
  labels: xArray,
  values: yArray,
  type: "pie"
}];
</pre>
<h1>Donut Graphs</h1>
<img src="https://i.imgur.com/jAfla3G.png" width="69%">
<pre>
var data = [{
  labels: xArray,
  values: yArray,
  hole: .4,
  type: "pie"
}];
</pre>
<h1>Math Graphs</h1>
<img src="https://i.imgur.com/RISdDm2.png" width="69%">
<pre>
var exp = "Math.sin(x)";
// Generate values
var xValues = [];
var yValues = [];
for (var x = 0; x <= 10; x += 0.1) {
  yValues.push(eval(exp));
  xValues.push(x);
}
// Display using Plotly
var data = [{x:xValues, y:yValues, mode:"lines"}];
var layout = {title: "y = " + exp};
Plotly.newPlot("myPlot", data, layout);
</pre>
<h1>Another Math Graphs</h1>
<img src="https://i.imgur.com/S9yhvaV.png" width="69%">
<pre>
var exp = "Math.cos(x)";
// Generate values
var xValues = [];
var yValues = [];
for (var x = 0; x <= 10; x += 0.2) {
  yValues.push(eval(exp));
  xValues.push(x);
}
// Display using Plotly
var data = [{x:xValues, y:yValues, mode:"markers"}];
var layout = {title: "y = " + exp};
Plotly.newPlot("myPlot", data, layout);
</pre>
