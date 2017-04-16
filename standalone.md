<script src="http://cdnjs.cloudflare.com/ajax/libs/d3/3.5.5/d3.min.js"></script>
<script src="https://wzrd.in/standalone/function-plot@1.13.0"></script>

<script src="https://cdn.plot.ly/plotly-latest.min.js"></script>

<div id="tester" style="width:600px;height:250px;"></div>

<script>
	TESTER = document.getElementById('tester');
	Plotly.plot( TESTER, [{
	x: [1, 2, 3, 4, 5],
	y: [1, 2, 4, 8, 16] }], {
	margin: { t: 0 } } );
</script>


<script>
 (function () {
   var functionPlot = window.functionPlot;

   functionPlot.globals.DEFAULT_WIDTH = 600;
   functionPlot.globals.DEFAULT_HEIGHT = 350;

   functionPlot({
     target: '#geometric-representation',
     yDomain: [-1, 9],
     data: [{
       fn: 'x * x'
     }]
   });
</script>

 <div id="geometric-representation">
