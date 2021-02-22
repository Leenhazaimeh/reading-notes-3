
# Canvas Element

  

HTML <canvas> tag is used to draw graphics on a web page usually via scripting (JS). The element is only a container for graphics. You must use a script to actually draw the graphics.

  

See this example:

`
	<canvas  id="myCanvas"  width="200"  height="100">		</canvas>
`
  

The width and height attribute is necessary to define the size of the canvas or it can be set to default which is 300px width and 150 px height.

  

to start drawing you should:

1. find the canvas element first, which is done by using DOM methods.

2. we need a drawing object for the canvas.

  

`
	var ctx = canvas.getContext("2d");
`

3. Finally, you can start drawing on the canvas. for example using fillRect(x,y,width,height) method which draws a rectangle.

  
  

then we can add colors using: fillStyle ( can be a CSS color, a gradient, or a pattern. ) and strokeStyle.

  

To draw text on a canvas,we need to either:

1. define the font properties for the text

2. fillText which draws filled text

3. StrokeText which draws text without fill

  

Note: We can use chart.js for charts by downloading it chart.min.js and use it into our directory and import the script in our HTML page.but we need to create canvas element in the body of the page then start the script that will retrieve the context of the canvas using script tags in the foot of our body , then inside the same script we need to create our data