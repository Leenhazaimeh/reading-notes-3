# CSS 

CSS stands for cascading style sheets. it's a way for styling your HTML content simply by calling the element we want to apply the style on it by sth called selectors then make a declaration with a property and a value for it.

Examples of selectors: 
- Tag name 
- class name 
- id 
- + 
- ~

your CSS code will look sth like this: 


``

	h1 {

	color:white;

	padding:20px;

	}

``
There are multiple ways of adding css styles to a web page: 
1. Inline (style attribute inside HTML element 'rarely used')
2. Internal (style tag inside head of the HTML 'used when you want to add styles to a web page that is different than others)
3. External (linking to a css file using link element in the head 'recommended and mostly used since it has many benifits such as: you don't have to modify each web page indivisually you simply can link every web page to the same css files & it helps also with performance since you don't have to add code to your HTML for each page to not download each css seperately.')


### Colors in CSS
We don't doubt that colors add life to everything, your web page should also have colors. 

Many ways of declaring colors by:
1. name 
2. rgb or rgba which is with opacity (can take values up to 255 , 0-1 for a)
3. HEX #00ffee where each two sequent numbers stands for rgb. 
4. HSLA which is hue,saturation,brightness and opacity (0-360,percentage,percentage,0-1)
