<h1>Basic</h1>
Create a tooltip that appears when the user moves the mouse over an element:
<pre>
&lt;style&gt;
/* Tooltip container */
.tooltip {
  position: relative;
  display: inline-block;
  border-bottom: 1px dotted black; /* If you want dots under the hoverable text */
}
/* Tooltip text */
.tooltip .tooltiptext {
  visibility: hidden;
  width: 120px;
  background-color: black;
  color: #fff;
  text-align: center;
  padding: 5px 0;
  border-radius: 6px;
  /* Position the tooltip text - see examples below! */
  position: absolute;
  z-index: 1;
}
/* Show the tooltip text when you mouse over the tooltip container */
.tooltip:hover .tooltiptext {
  visibility: visible;
}
&lt;/style&gt;
&lt;div class="tooltip"&gt;Hover over me
  &lt;span class="tooltiptext"&gt;Tooltip text&lt;/span&gt;
&lt;/div&gt;
</pre>
<b><i>Explained:</i></b>
<br>
<b>HTML:</b> Use a container element (like <b>&lt;div&gt;</b>) and add the "tooltip" class to it. When the user mouse over this <b>&lt;div&gt;</b>, it will show the tooltip text.
<br>
The tooltip text is placed inside an inline element (like <b>&lt;span&gt;</b>) with class="tooltiptext".
<br>
<b>CSS:</b> The tooltip class use position:relative, which is needed to position the tooltip text (position:absolute). Note: See examples below on how to position the tooltip.
<br>
The tooltiptext class holds the actual tooltip text. It is hidden by default, and will be visible on hover (see below). We have also added some basic styles to it: 120px width, black background color, white text color, centered text, and 5px top and bottom padding.
<br>
The CSS border-radius property is used to add rounded corners to the tooltip text.
<br>
The :hover selector is used to show the tooltip text when the user moves the mouse over the <b>&lt;div&gt;</b> with class="tooltip".
<h1>Positioning</h1>
In this example, the tooltip is placed to the right (<b>left:105%</b>) of the "hoverable" text (<b>&lt;div&gt;</b>). Also note that <b>top:-5px</b> is used to place it in the middle of its container element. We use the number 5 because the tooltip text has a top and bottom padding of 5px. If you increase its padding, also increase the value of the <b>top</b> property to ensure that it stays in the middle (if this is something you want). The same applies if you want the tooltip placed to the left.
<pre>
.tooltip .tooltiptext {
  top: -5px;
  left: 105%;
}
</pre>
<pre>
.tooltip .tooltiptext {
  top: -5px;
  right: 105%;
}
</pre>
If you want the tooltip to appear on top or on the bottom, see examples below. Note that we use the margin-left property with a value of minus 60 pixels. This is to center the tooltip above/below the hoverable text. It is set to the half of the tooltip's width (120/2 = 60).
<pre>
.tooltip .tooltiptext {
  width: 120px;
  bottom: 100%;
  left: 50%;
  margin-left: -60px; /* Use half of the width (120/2 = 60), to center the tooltip */
}
</pre>
<pre>
.tooltip .tooltiptext {
  width: 120px;
  top: 100%;
  left: 50%;
  margin-left: -60px; /* Use half of the width (120/2 = 60), to center the tooltip */
}
</pre>
<h1>Arrows</h1>
To create an arrow that should appear from a specific side of the tooltip, add "empty" content after tooltip, with the pseudo-element class <b>::after</b> together with the <b>content</b> property. The arrow itself is created using borders. This will make the tooltip look like a speech bubble.
<br>
This example demonstrates how to add an arrow to the bottom of the tooltip:
<pre>
.tooltip .tooltiptext::after {
  content: " ";
  position: absolute;
  top: 100%; /* At the bottom of the tooltip */
  left: 50%;
  margin-left: -5px;
  border-width: 5px;
  border-style: solid;
  border-color: black transparent transparent transparent;
}
</pre>
<b>Explained:</b>
<br>
Position the arrow inside the tooltip: <b>top: 100%</b> will place the arrow at the bottom of the tooltip. <b>left: 50%</b> will center the arrow.
<br>
<b><i>Note:</i></b> The <b>border-width</b> property specifies the size of the arrow. If you change this, also change the <b>margin-left</b> value to the same. This will keep the arrow centered.
<br>
The border-color is used to transform the content into an arrow. We set the top border to black, and the rest to transparent. If all sides were black, you would end up with a black square box.
<br>
This example demonstrates how to add an arrow to the top of the tooltip. Notice that we set the bottom border color this time:
<pre>
.tooltip .tooltiptext::after {
  content: " ";
  position: absolute;
  bottom: 100%;  /* At the top of the tooltip */
  left: 50%;
  margin-left: -5px;
  border-width: 5px;
  border-style: solid;
  border-color: transparent transparent black transparent;
}
</pre>
This example demonstrates how to add an arrow to the left of the tooltip:
<pre>
.tooltip .tooltiptext::after {
  content: " ";
  position: absolute;
  top: 50%;
  right: 100%; /* To the left of the tooltip */
  margin-top: -5px;
  border-width: 5px;
  border-style: solid;
  border-color: transparent black transparent transparent;
}
</pre>
This example demonstrates how to add an arrow to the right of the tooltip:
<pre>
.tooltip .tooltiptext::after {
  content: " ";
  position: absolute;
  top: 50%;
  left: 100%; /* To the right of the tooltip */
  margin-top: -5px;
  border-width: 5px;
  border-style: solid;
  border-color: transparent transparent transparent black;
}
</pre>
<h1>Fade in</h1>
If you want to fade in the tooltip text when it is about to be visible, you can use the CSS <b>transition</b> property together with the <b>opacity</b> property, and go from being completely invisible to 100% visible, in a number of specified seconds (1 second in our example):
<pre>
.tooltip .tooltiptext {
  opacity: 0;
  transition: opacity 1s;
}
.tooltip:hover .tooltiptext {
  opacity: 1;
}
</pre>
