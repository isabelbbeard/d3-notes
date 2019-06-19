# d3 Guide

- [Atom](#atom)
- [HTML5](#atom)
- [CSS](#css)


## Atom(#atom)
It's useful to have some sort of code editor, [Atom](https://atom.io/) is really nice and allows you to add plugins to help with workflow.

## HTML5(#html5)
[HTML5](https://www.w3.org/TR/html52/) website is a great reference and has all information you'll need.

### Structuring HTML5 Documents
HTML5 is essential a structure document outlines.
![html structure](https://github.com/isabelbbeard/d3-notes/blob/master/images/Screenshot%202019-06-19%20at%2010.35.12.png)

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

## CSS(#css)

another test
