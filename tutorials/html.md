# HTML

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
  

### CSS
 
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
   
   
   
