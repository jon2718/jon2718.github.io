---
layout: default
---

## Welcome to another page



_yay_

[back](./)


<head>
 <link rel="stylesheet" type="text/css" href="https://jsxgraph.uni-bayreuth.de/distrib/jsxgraph.css" />
 <script type="text/javascript" src="https://jsxgraph.uni-bayreuth.de/distrib/jsxgraphcore.js"></script>
</head>

<div id="box" class="jxgbox" style="width:500px; height:500px;"></div>
<script type="text/javascript">
 var b = JXG.JSXGraph.initBoard('box', {boundingbox: [-10, 10, 10, -10], axis:true});
 var p1 = b.createElement('point',[0,0], {name:'A',size: 4, face: 'o'});
 var p2 = b.createElement('point',[2,-1], {name:'B',size: 4, face: 'o'});
 var ci = b.createElement('circle',["A","B"], {strokeColor:'#00ff00',strokeWidth:2});
</script>

<script src="https://d3js.org/d3.v4.js"></script>
<div id="viz"></div>
   <script type="text/javascript">

   var sampleSVG = d3.select("#viz")
       .append("svg")
       .attr("width", 100)
       .attr("height", 100);    

   sampleSVG.append("circle")
       .style("stroke", "gray")
       .style("fill", "white")
       .attr("r", 40)
       .attr("cx", 50)
       .attr("cy", 50)
       .on("mouseover", function(){d3.select(this).style("fill", "aliceblue");})
       .on("mouseout", function(){d3.select(this).style("fill", "white");});

   </script>

<iframe width="1000" height="1000" frameborder="0" allowfullscreen>
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>My first HTML document</TITLE>
   </HEAD>
<BODY>

<script src="http://cdnjs.cloudflare.com/ajax/libs/d3/3.5.5/d3.min.js"></script>
<script src="https://wzrd.in/standalone/function-plot@1.13.0"></script>

 <div id="complex-plane">
 <div class="center">$1, i, -1, -i$</div>


<script>
 (function () {
   var functionPlot=window.functionPlot;
   functionPlot.globals.DEFAULT_WIDTH=600;
   functionPlot.globals.DEFAULT_HEIGHT=350;
   var instance = functionPlot({
     target: '#complex-plane',
     xLabel: 'real',
     yLabel: 'imaginary',
     grid: true,
     xDomain: [-6, 6],
     data: [
       vector([1, 0]),
       vector([0, 1]),
       vector([-1, 0]),
       vector([0, -1]),
       unitCircle()
     ]
   })
   updateFormat(instance)
 })()
 </script>

</BODY>
</iframe>
