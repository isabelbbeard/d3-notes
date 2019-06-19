# d3 Guide

- [Atom](#atom)
- [HTML5](#html5)
- [CSS](#css)
- [Javascript](#Javascript)
- [D3](#d3)


## Atom
It's useful to have some sort of code editor, [Atom](https://atom.io/) is really nice and allows you to add plugins to help with workflow.

## HTML5
[HTML5](https://www.w3.org/TR/html52/) website is a great reference and has all information you'll need.

### Structuring HTML5 Documents
HTML5 is essential a structure document outlines.
![html structure](https://github.com/isabelbbeard/d3-notes/blob/master/images/Screenshot%202019-06-19%20at%2010.35.12.png)

DOM, is the Document Object Model

Sectioning elements
- `article`, `aside`, `nav` and `section`
- Each time one of these elements is used, a new section is created

Grouping
- `footer`, `header` and `main`
- Used to group sections

### Starting a Documents

#### Boiler Plate
Start a document structure (boiler plate):
```HTML5
<!doctype html> <!-- You need to declare the doctype as html -->
<html lang = "en">

  <head>
      <!-- Your comment here -->
      <meta charset="utf-8">
      <title> Page title here </title><!-- Add a page title in the <head> -->
  </head>

  <body>
    <header><!-- branding and navigation go here--></header >
  </body>

  <footer><!-- disclaimer and contact info go here--></footer>

</html>
```
### Additional content

#### Article
Articles are stand alone content (like an article of clothing) - can be removed from the page and still understandable.
```HTML5
<article>  
  <!-- main review go here-->
</article>
```

#### Section
Groups themed content together. All content within is related. (Like a section of contents). Or a section within an article.
```HTML5
<section><!-- comments go here--></section>
```

#### Aside
Aside content is related to it’s siblings but isn’t really important enough to be it’s own article.
```HTML5
<aside><!-- ad copy go here--></aside>
```

### Emphasizing text
```HTML5
<i></i> <!-- Italic is for a span of text in an alternate voice or mood -->
<em></em> <!-- Represents stress emphasis of its elements -->
<b></b> <!-- Represents a span of text to which attention is being drawn for utilitarian purposes without conveying extra importance and with no implication of an alternate voice or mood -->
<strong></strong> <!-- Represents strong importance or seriousness -->
```

### Attributes
All HTML elements can be assigned attributes by including property/value pairs in the opening tag.
```HTML5
<tagname property = "value"></tagname>
```

### Classes and IDs
Classes and IDs can be references later to identify specific pieces of content.
You can have multiple classes by separating with a space.
```HTML5
<p class = "class1"> content <p>
<p class = "class1"> content <p>
<p class = "class1 class2"> content <p>
```
You can only have one ID per element. Ids are useful when a single element has some special quality.
```HTML5
<div id = 'content'>
	<div id = "visualization></div>
	<div ide = "button"></div>
</div>
```

### Structuring content

#### Main
Main is a semantic element says that everything inside me is the main content on the page. Can include other elements.
```HTML5
<main>
  <article>  
    <!-- main review go here-->
    <section><!-- comments go here--></section>
  </article>
</main>
```

#### Headings
Headings create new sections.
Use H1 per page (in the <header> section). It is the main header of the document.
```HTML5
<H1>Page header here</H1>
<H2>Another heading level</H2>
```

#### Paragraphs
```HTML5
<p> Text goes here for a paragraph </p>
```

## CSS
Cascading Style Sheets are used to style the visual presentation of DOM elements. CSS styles consist of ‘selectors’ and ‘properties’. Selectors are followed by properties, grouped in curly brackets. A property and its value are separated by a colon, and the line is terminated with a semicolon, like the following.

```CSS
selectorA,
selectorB {
	property: value;
	property: value;
	property: value;
}
```
You can assign the same properties to multiple selectors by separating selectors with commas.

An example of real css (or a css rule):

```CSS
p,
li {
	font-size: 12px;
	line-height: 14px;
	Color: orange;
}
```

### Selectors
D3 uses CSS-style selectors to identify elements on which to operate. Selectors identify specific elements to which styles will be applied.

#### Type selectors
```CSS
h1		   /* Selects all level 1 headings		*/
p		     /* Selects all paragraphs		   		*/
strong	 /* Selects all strong elements			*/
em 		   /* Selects all em elements		  	 	*/
div		   /* Selects all divs				      	*/
```

#### Descendent selectors
These match elements that are contained by or ‘descended from’ another element.
```CSS
h1 em		 /* Selects all em elements contained in an h1	*/
div p		 /* Selects all p elements contained in a div	*/
```

#### Class selectors
These match elements of any type that have been assigned a specific class.
```CSS
.caption  	 /* Selects elements with class 'caption'			*/
.label    	/* Selects elements with class 'label'			*/
.axis.x   	/* Selects elements with class 'axis' and class ‘x’	*/
```

#### ID selectors
These match the single element with a given ID. Id’s can only be used once.
```CSS
#header	  /*Selects element with ID 'header'		*/
#nav	  	/*Selects element with ID 'nav		*/
#export 	/*Selects element with ID 'export'		*/
```

[List](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference) of CSS properties.

### Referencing Styles

#### Embed CSS in your HTML
```html5
<html>
  <head>
    <style type = "text/css">
      p {
        font-size: 24px;
        font-weight: bold;
        background-color: red;
        color: white;
      }
    </style>
  </head>
  <body>
      <p>testing here</p>
  </body>
</html>
```

#### Reference an external stylesheet from the HTML
```html5
<html>
  <head>
    <link rel = "stylesheet" href = "style.css"
  </head>
  <body>
      <p>testing here</p>
  </body>
</html>
```

#### Attach inline styles
```html5
<p style = "color:blue; font-size: 48px; font-style:italic;">testing here</p>
```

## Javascript
JavaScript is the language that can make pages dynamic by manipulating the DOM after a page has already loaded in the browser.

Print something in the console:
```JavaScript
console.log('something');
```

#### Variables
Variables are containers for data. A simple variable holds one value:
```JavaScript
var number = 5;
```

#### Arrays
An array is a sequence of values stored in one variable.
```JavaScript
var numbers = [5, 10, 15, 20]
Numbers[2]
>> 15
```

#### Objects
Objects are a custom data structure. Use curly brackets to indicate an object. In between the brackets, there are properties and values.
```JavaScript
var fruit = {
	kind: "orange",
	color: "red",
	quantity: 12
};

fruit.kind
>> "orange"
```

#### If (only)
An if statements uses comparison operators to determine if a statement is true or false:
```JavaScript
if (3 < 5) {
	console.log("woohoo");
}
```
#### for() now
For loops repeatedly execute the same code with slight variations:
```JavaScript
for (var i = 0; i < 5; i++){
	console.log(i)
}
```
#### Functions
Functions are chunks of code that can do things. An example of a made-up function:
```JavaScript
var calculateGratuity = function(bill) {
	Return bill * 0.2;
}

calculateGratuity(38);
>> 7.6
```

## D3

- Great series of tutorials on [youtube](https://www.youtube.com/watch?v=n5NcCoa9dDU&list=UUNYL0ZF2j8-OSGZ4iHBLNPA&index=20).
- [Examples of d3](https://github.com/d3/d3/wiki/Gallery)
- [Documentation of d3](https://github.com/d3/d3/blob/master/API.md)

Adding d3 to a Document
```html5
<script src = 'http://d3js.org/d3.v3.min.js'></script>
```
Adding a d3 element within the body
```html5
<script>
      // d3.select("p").text("Hello World");
      d3.select("body") //.select selecs an elements
        .append("p")  //.append adds elements
        .style("color", "red") //.style affects the css of the item
        .text("Hi, Whats Up?")
</script>
```
### Creating some svg shapes (within a script tag)

```JavaScript
var canvas = d3.select("body")
                .append("svg") //adds svg element to the pages
                .attr("width", 500) //when styling svg elements we use attribute method instead of style
                .attr("height", 500); //always end with semicolon

var circle = canvas.append("circle")
                  .attr("cx", 250)
                  .attr("cy", 250)
                  .attr("r", 50)
                  .attr("fill", "blue");

var rect = canvas.append("rect")
                  .attr("width", 50)
                  .attr("height", 150)
                  .attr("fill", "red");

var line = canvas.append("line")
                .attr("x1", 0)
                .attr("y1", 100)
                .attr("x2", 400)
                .attr("y2", 400)
                .attr("stroke", "green")
                .attr("stroke-width", 10);

```
![svg shapes](https://github.com/isabelbbeard/d3-notes/blob/master/images/Screenshot%202019-06-19%20at%2012.02.53.png)

### Create simple bars using data
See code here to create this output:
