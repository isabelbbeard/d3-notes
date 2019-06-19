# d3 Guide

## Atom
It's useful to have some sort of code editor, [Atom](https://atom.io/) is really nice and allows you to add plugins to help with workflow.

## HTML5
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

#### Doctype
You need to declare the doctype:

```HTML5
<!doctype html>
```

#### Boiler Plate
Start a document structure (boiler plate):
```HTML5
<!doctype html>
<html lang = "en">

  <head>
      <meta charset="utf-8">
  </head>

  <body>
  </body>

</html>
```

#### Comments
comments are written as:
```HTML5
<!-- Your comment here -->
```

#### Title
Add a page title in the <head>
```HTML5
<title> Page title here </title>
```

#### Header
Header is usually where logo navigation sits and is inside the <body>
```HTML5
<body>
  <header><!-- branding and navigation go here--></header >
</body>
```
