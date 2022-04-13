<a href="/JS/Graphics/Google-Chart.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/Quiz.md">Next &gt;</a>
<hr>
D3.js is a JavaScript library for manipulating HTML data.
<br>
D3.js is easy to use.
<h1>How to Use it?</h1>
To use D3.js in your web page, add a link to the library:
<pre>&lt;script src="//d3js.org/d3.v3.min.js"&gt;&lt;/script&gt;</pre>
This script selects the body element and appends a paragraph with the text "Hello World!":
<pre>d3.select("body").append("p").text("Hello World!");</pre>
<h1>Scatter Graphs</h1>
<img src="https://i.imgur.com/cgqWwyM.png" width="69%">
<pre>
// Set Dimensions
const xSize = 500;
const ySize = 500;
const margin = 40;
const xMax = xSize - margin*2;
const yMax = ySize - margin*2;
// Create Random Points
const numPoints = 100;
const data = [];
for (let i = 0; i < numPoints; i++) {
  data.push([Math.random() * xMax, Math.random() * yMax]);
}
// Append SVG Object to the Page
const svg = d3.select("#myPlot")
  .append("svg")
  .append("g")
  .attr("transform","translate(" + margin + "," + margin + ")");
// X Axis
const x = d3.scaleLinear()
  .domain([0, 500])
  .range([0, xMax]);
svg.append("g")
  .attr("transform", "translate(0," + yMax + ")")
  .call(d3.axisBottom(x));
// Y Axis
const y = d3.scaleLinear()
  .domain([0, 500])
  .range([ yMax, 0]);
svg.append("g")
  .call(d3.axisLeft(y));
// Dots
svg.append('g')
  .selectAll("dot")
  .data(data).enter()
  .append("circle")
  .attr("cx", function (d) { return d[0] } )
  .attr("cy", function (d) { return d[1] } )
  .attr("r", 3)
  .style("fill", "Red");
</pre>
