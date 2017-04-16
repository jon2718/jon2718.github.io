<script src="http://cdnjs.cloudflare.com/ajax/libs/d3/3.5.5/d3.min.js"></script>
<script src="https://wzrd.in/standalone/function-plot@1.13.0"></script>


 <div id="geometric-representation">
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
