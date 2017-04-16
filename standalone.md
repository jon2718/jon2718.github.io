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
