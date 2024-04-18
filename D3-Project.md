---
author: Lucas Williams
copyright: Lucas Williams
title: What is D3 in web development
---

# D3 (Data-Driven Documents)

D3, also referred to as Data-Driven Documents, is a JavaScript library used for manipulating documents based on data. D3 allows its users to transform text into visualizations using HTML, SVG, and CSS. It is frequently used for growing interactive visualizations in web browsers, allowing for better data comprehension for end users.

## Purpose

The purpose of using D3 is to create a dynamic and interactive visualization on a website using the data. D3 enables developers to bind data to a DOM, also known as a Document Object Model, element and then apply some data-driven changes to the visualization of the document.

## Installation and Setup

To begin using D3 you will first need to install d3 using npm or by using a script tag in the website.

The installation command via npm is:

```
npm install d3
```
Alternatively, you can include it directly in your HTML file using a script tag:

```html
<script src="https://d3js.org/d3.v7.min.js"></script>
```

## Some examples of using D3

# This is how you make a bar chart

```
// HTML
<div id="chart"></div>

// JavaScript
var data = [10, 20, 30, 40, 50];

var svg = d3.select("#chart")
            .append("svg")
            .attr("width", 400)
            .attr("height", 200);

svg.selectAll("rect")
   .data(data)
   .enter()
   .append("rect")
   .attr("x", function(d, i) { return i * 80; })
   .attr("y", function(d) { return 200 - d; })
   .attr("width", 40)
   .attr("height", function(d) { return d; })
   .attr("fill", "blue");
```

# Description:
Creates a simple bar chart using SVG elements.
Each rectangle represents a data point.
The height of each rectangle corresponds to the data value.
The fill attribute sets the color of the bars.

# This is how you make a scatter plot

```
// HTML
<div id="scatterplot"></div>

// JavaScript
var data = [
    { x: 10, y: 20 },
    { x: 20, y: 30 },
    { x: 30, y: 40 },
    { x: 40, y: 50 },
    { x: 50, y: 60 }
];

var svg = d3.select("#scatterplot")
            .append("svg")
            .attr("width", 400)
            .attr("height", 200);

svg.selectAll("circle")
   .data(data)
   .enter()
   .append("circle")
   .attr("cx", function(d) { return d.x; })
   .attr("cy", function(d) { return d.y; })
   .attr("r", 5)
   .attr("fill", "red");
```

# Description:
Constructs a scatter plot using SVG circles.
Each circle represents a data point with an x and y coordinate.
The cx and cy attributes determine the position of each circle.
The r attribute sets the radius of the circles.

# This is how you make a line chart

```
// HTML
<div id="linechart"></div>

// JavaScript
var data = [10, 20, 30, 40, 50];

var svg = d3.select("#linechart")
            .append("svg")
            .attr("width", 400)
            .attr("height", 200);

var line = d3.line()
             .x(function(d, i) { return i * 80; })
             .y(function(d) { return 200 - d; });

svg.append("path")
   .datum(data)
   .attr("d", line)
   .attr("fill", "none")
   .attr("stroke", "blue");
```

# Description:
Generates a basic line chart using SVG path elements.
The line function constructs the path based on the data.
The datum method binds the data to the path.
The fill and stroke attributes define the appearance of the line.

## Resources

[GitHub D3 Documentation](https://github.com/d3/d3/wiki)
[D3 Graph Documentation](https://www.d3-graph-gallery.com/)
[Official D3 Website](https://d3js.org/)
