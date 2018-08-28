# HTML

## Table of contents

* [Learning resources](#learning-resources)
* [Basics you need to know](#basics-you-need-to-know)
  * [HTML tags](#html-tags)
  * [HTML attributes](#html-attributes)
  * [File paths](#file-paths)
  * [Typical structure of HTML document](#typical-structure-of-html-document)
  * [CSS in HTML](#css-in-html)
  

## Learning resources

1 **W3Schools**: https://www.w3schools.com/html/default.asp  


## Basics you need to know

### HTML tags

These are the most often used HTML tags:  

* Used once per `.html` file: 
  * `<html>`, `<head>`, `<body>`  
* Used many times: 
  * `<div>`, `<h1>`, `<h2>`, `<h3>`, `<p>`, `<span>`, `<b>`, `<i>`, `<u>`, `<ul>`, `<li>`, `<blockquote>`, `<a>`  
* Semantic Tags (often used just once, but can be used many times): 
  * `<nav>`, `<header>`, `<section>`, `<footer>`  
* `<head>` tags (used many times):  
  * `<meta>`, `<link>`, `<script>`
  

### HTML attributes

These are the most often used HTML attributes:  

* Used across many tags:
  * `id=""`, `class=""`, `title=""`, `style=""` 
* Used with `<img`> tag:  
  * `src=""`, `alt=""` 
* Used with `<a>` tag:  
  * `href=""`  
  
  
### File paths

This one is important.  
Pay attention to the table with 4 examples: https://www.w3schools.com/html/html_filepaths.asp


### Typical structure of HTML document

Feel free to copy/paste it, and use as a skeleton for your web pages.   

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Document</title>
</head>
<body>

  <nav>
    <!-- Navigation bar
    Links to web pages of your site will go here... -->
  </nav>
  
  <header>
    <!-- Header
    Typically a widescreen-style banner for your web site.
    It may include a call-to-action button:
    https://blog.hubspot.com/marketing/call-to-action-examples -->
  </header>
  
  <section>
    <!-- A Section
    Contents of your web page should be divided into Sections
    You will likely have many of those on a web page -->
  </section>
  
  <footer>
    <!-- Footer
    Footers typically include information such as:
    social media links,
    information about the company,
    address,
    a list of links,
    Privacy Policy, Code of Conduct, and links to other legal documents -->
  </footer>
  
</body>
</html>
```

### CSS in HTML
 
There are three (3) ways to use CSS in HTML:  
 
* Inline
  * example: `<h1 style="color:blue;">This is a Blue Heading</h1>`
  * use it when you know you will be styling only one tag this way. Otherwise, create a CSS class rule, and use the class throughout several HTML tags.
* Internal
  * example: ```<style>
    body {background-color: powderblue;}
    h1   {color: blue;}
    p    {color: red;}
    </style>```
  * use it when defined rules will apply only to one `.html` file. Otherwise, use an external CSS file (see below).
* External
  * example: `<link rel="stylesheet" href="styles.css">`
  * use it as default. Your CSS rules will live in an external file (e.g. `styles.css`), and many `.html` files will be able to link to it using `<link>` tag. It allows you to reuse your CSS rules (**reusability**).
   
   
   
