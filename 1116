function 161116()
{
var width = 800;
var height = 600;
var ctrl = d3.select(".header").append("svg").attr("width", width).attr("height", height);
d3.csv("https://minyiyou.github.io/hello/haha.csv", 
	function(data)
	{
		var ln = data.length;
		console.log(data);
		var maxy = d3.max(data, function(d){ return d.sold; });
		var miny = d3.min(data, function(d){ return d.buy; });
		var lines = d3.line().x(function(d,i){return (ln-i)*(width/ln);})
		.y(function(d){return height-(d.sold-miny)*(height/(maxy-miny))});
		var line2 = d3.line().x(function(d,i){return (ln-i)*(width/ln);})
		.y(function(d){return height-(d.buy-miny)*(height/(maxy-miny))});
		ctrl.append("path").data([data]).attr("d", lines).attr("stroke", "red").attr("fill", "none");
        ctrl.append("path").data([data]).attr("d", line2).attr("stroke", "green").attr("fill", "none");
        
	}

);
}