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


<div id="my-graph" style="width:600px;height:250px;"></div>

<script>
Plotly.d3.csv('https://raw.githubusercontent.com/plotly/datasets/master/gapminderDataFiveYear.csv', function(err, rows){
var YEAR = 2007;
var continents = ['Asia', 'Europe', 'Africa', 'Oceania', 'Americas'];
var POP_TO_PX_SIZE = 2e5;
function unpack(rows, key) {
  return rows.map(function(row) { return row[key]; });
}

var data = continents.map(function(continent) {
  var rowsFiltered = rows.filter(function(row) {
      return (row.continent === continent) && (+row.year === YEAR);
  });
  return {
      mode: 'markers',
      name: continent,
      x: unpack(rowsFiltered, 'lifeExp'),
      y: unpack(rowsFiltered, 'gdpPercap'),
      text: unpack(rowsFiltered, 'country'),
      marker: {
          sizemode: 'area',
          size: unpack(rowsFiltered, 'pop'),
          sizeref: POP_TO_PX_SIZE
      }
  };
});
var layout = {
  xaxis: {title: 'Life Expectancy'},
  yaxis: {title: 'GDP per Capita', type: 'log'},
  margin: {t: 20},
  hovermode: 'closest'
};
Plotly.plot('my-graph', data, layout, {showLink: false});
});
</script>


<div id="matlab-basic-line" style="width:600px;height:250px;"></div>

<script>
x = linspace(-2*pi,2*pi);
y1 = sin(x);
y2 = cos(x);

fig = figure;
plot(x,y1,x,y2);

%--PLOTLY--%

% Strip MATLAB style by default!
response = fig2plotly(fig, 'filename', 'matlab-basic-line');
plotly_url = response.url;

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
