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
