# D3 (Data-Driven-Documents)

* D3 is an extremely powerful visualization tool to create interactive data visualizations.
* D3 is **data driven**. It can use static data or fetch it from the remote server in different formats such as Arrays, Objects, CSV, JSON, XML etc. to create different types of charts.
* DOM Manipulation, Dynamic Properties,Custom Visualizations,Transitions,Interaction and animation.

#### Advantages of D3
* D3 is an open-source javascript library and can be used in any framework as it is light-weight.


##### Create a Linear Scale with D3

* The bar and scatter plot charts both plotted data directly onto the SVG canvas. However, if the height of a bar or one of the data points were larger than the SVG height or width values, it would go outside the SVG area.
* In D3, there are scales to help plot data. ***Scales*** are functions that tell the program how to map a set of raw data points onto the pixels of the SVG canvas.
* By default, scales use the identity relationship. This means the input value maps to the output value.
* Say a *dataset has values ranging from 50 to 480. This is the input information for a scale*, also known as the **domain**.
* You want to *map those points along the x axis on the SVG canvas, between 10 units and 500 units. This is the output information*, also known as the **range**.
* The **domain()** method passes information to the scale about the raw data values for the plot. 
* The **range()** method gives it information about the actual space on the web page for the visualization.
* D3 has several scale types:
    * ScaleLinear: const scale = d3.scaleLinear();
    * 
##### Data Visualization with D3: Use a Pre-Defined Scale to Place Elements
D3 has two methods, axisLeft() and axisBottom(), to render the y-axis and x-axis, respectively. Here's an example to create the x-axis based on the xScale in the previous challenges:

const xAxis = d3.axisBottom(xScale);
The next step is to render the axis on the SVG canvas. To do so, you can use a general SVG component, the g element. The g stands for group. Unlike rect, circle, and text, an axis is just a straight line when it's rendered. Because it is a simple shape, using g works. The last step is to apply a transform attribute to position the axis on the SVG canvas in the right place. Otherwise, the line would render along the border of SVG canvas and wouldn't be visible. SVG supports different types of transforms, but positioning an axis needs translate. When it's applied to the g element, it moves the whole group over and down by the given amounts. Here's an example:

const xAxis = d3.axisBottom(xScale);

svg.append("g")
   .attr("transform", "translate(0, " + (h - padding) + ")")
   .call(xAxis);
The above code places the x-axis at the bottom of the SVG canvas. Then it's passed as an argument to the call() method. The y-axis works in the same way, except the translate argument is in the form (x, 0). Because translate is a string in the attr() method above, you can use concatenation to include variable values for its arguments.
