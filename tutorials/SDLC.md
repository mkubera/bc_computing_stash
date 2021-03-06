# SDLC (Software Development LifeCycle)

## Table of Contents

* [Software Development LifeCycle](#software-development-lifecycle)
* [Sequential and Iterative and Incremental development](#sequential-and-iterative-and-incremental-development)
  * [Cheat sheet](#cheat-sheet)
  * [Agile](#agile)
  * [Waterfall](#waterfall)
  * [Spiral](#spiral)
* [Prototype revolutionary vs evolutionary](#prototype-revolutionary-vs-evolutionary)
  * [Revolutionary prototyping](#revolutionary-prototyping)
  * [Evolutionary prototyping](#evolutionary-prototyping)
* [Requirements](#requirements)
  * [Functional requirements](#functional-requirements)
  * [Non functional requirements](#non-functional-requirements)
  * [Examples of functional requirements of a web app](#examples-of-functional-requirements-of-a-web-app)
  * [Examples of non functional requirements of a web app](#examples-of-non-functional-requirements-of-a-web-app)
* [Planning](#planning)
  * [Brief](#brief)
* [Design](#design)
  * [Wireframes](#wireframes)
  * [Full designs](#full-visual-designs)
  * [Navigation map](#navigation-map)
  * [Flowcharts](#flowcharts)
* [Types of testing](#types-of-testing)
  *  [Alpha testing](#alpha-testing)
  *  [Beta testing](#beta-testing)
  *  [White box testing](#white-box-testing)
  *  [Black box testing](#black-box-testing)
  *  [Black box vs white box testing](#black-box-vs-white-box-testing)
  *  [Usability testing](#usability-testing)
  *  [Automated unit testing](#automated-unit-testing)
* [Unified Modeling Language](#unified-modeling-language)
  * [UML](#uml)
  * [UML types of diagrams](#uml-types-of-diagrams)

## Software Development LifeCycle

In a nutshell, **SDLC** involves:  

1.	**Planning** (Analysis)
    * Brief
    *	Functional requirements
    *	Non-functional requirements
2.	**Design**
    *	Wireframes
    *	Full visual designs
    * Navigation map
    * Flow charts (Logic algorithms)
3.	**Implementation** (Construction)
    *	Coding
    *	Testing
4.	**Deploying**

Different companies do things differently, so you will find some minor differences between what I laid out above and what the linked graphic shows: http://www.mywebprogrammer.com/wp-content/uploads/2016/10/website-design-process.jpg, but these are good examples of what SDLCs commonly look like.  
In case you wondered, companies have their own unique SDLCs because these are not set in stone, but rather have to be tailored towards what works best for a specific group of developers.  


## Sequential and Iterative and Incremental development

### Cheat sheet 
**Sequential** means **Waterfall**  
**Iterative** means **Agile**  
**Incremental** means **Spiral**  

### Agile
**Agile** is a process often used in start-ups and modern tech companies. Its aim is to develop applications quickly and be able to adapt to changing requirements (from the client, for example) all the time.  
It’s called **iterative** because it’s developed in iterations. It starts as a small app (Planned, Designed, Developed, Tested), and then the team iterates over it to enhance it (again, Planning, Designing, Developing, Testing).  
Iteration allows to go back in the process, meaning that if the team makes a mistake in Cycle #1’s Planning stage, it can then easily iterate over the SDLC, and tweak things in Cycle #2’s Planning stage. Agile aims to flexible and developer-friendly.  
**Agile** is **a rapid** app development methodology.  
more on Agile: https://en.wikipedia.org/wiki/Agile_software_development  
Intro to Agile: https://www.youtube.com/watch?v=HlUNaC4sxm8  

A good example of an Agile approach that suits small-scale applications is SCRUM.  
more on SCRUM: 
* [Scrum @wikipedia](https://en.wikipedia.org/wiki/Scrum_(software_development))
* [Introduction to Scrum](https://www.youtube.com/watch?v=9TycLR0TqFA) (only watch 00:00-03:00)

### Waterfall
**Waterfall** is the old way of doing things, it’s still in use, but is falling out of fashion as it’s too slow to respond to software’s changing requirements.  
Simply put, it is called waterfall because it goes step by step (Planning, Designing, Developing, Testing) from top to bottom, but it never goes back in the process; meaning, if there’s a fault in Planning, but the team is already on Developing stage, waterfall doesn’t provide flexibility to go back to Planning, and fix things.  
As you can see, given the example above, waterfall is a crippled model for software development. Shortcomings of **Waterfall** prompted development teams to look for different solutions. **Agile** is a great example of one as it allows iterating over an App repeatedly.  
more on Waterfall: https://en.wikipedia.org/wiki/Waterfall_model  

### Spiral
**Spiral** is just Waterfall but repeated over and over again.  
Just like **Agile**, **Spiral** is a **rapid** app development methodology.  
more on Spiral: https://en.wikipedia.org/wiki/Spiral_model  

### Further reading
Read more about all three models here: https://apprenticeoscar.wordpress.com/2018/02/23/sequential-iterative-and-incremental/   
Read about Waterfall vs Spiral models of systems development + (dis)advantages here: https://techspirited.com/comparison-between-waterfall-model-spiral-model  


## Prototype revolutionary vs evolutionary

### Evolutionary prototyping
> Exploratory development where the objective of the process is to work with the customer to explore their requirements and deliver a final system. The development starts with the parts of the system that are understood. The system gradually evolves into a finished application by adding new features proposed by the customer.  

### Revolutionary prototyping
> Revolutionary, or "Throwaway", prototyping is where the objective is to understand the customer's requirements and hence develop a better requirements definition for the system. The prototype concentrates on experimenting with the customer requirements that are poorly understood. It is called "throwaway" because it is a model used to test only aspects of an application.  


## Planning

### Brief
> A design brief is a written document that summarizes all the relevant information about a project. As it includes an outlined strategy for the project, it’s an essential piece you need to have before starting any design work.  
>
> A brief sets the guidelines of a project, including background information, goals, requirements and technical directives so that every person involved in it can work towards the same purpose and find the information he needs in order to achieve it.  
>
> The word brief is defined as something “of short duration”. In other industries, like advertising, the brief is sometimes required to be as short as it can be. But the length of such a document will actually vary according to each designer, project and client. I wouldn’t worry about the length as long as it’s clear, understandable and provides the elements you need in order to take the project to a good end (no less, no more).  
>
> Typically, every web design project starts with a brief. Sometimes your client will send the first version with their requirements, but most of the times it’ll be you (the designer or the agency) who writes this kind of document.

**Learning materials**
* [How to Write a Website Design Brief](https://artisanthemes.io/write-website-design-brief/)
* [HeliosDesign Sample Website Brief](http://www.heliosdesign.co.za/export/sites/helios/content/common/HeliosDesign_Sample_Website_Brief.pdf)



## Design

### Wireframes
> A website wireframe is a visual guide that represents the skeletal framework of a website. The wireframe usually lacks typographic style, color, or graphics, since the main focus lies in functionality, behavior, and priority of content.

**Learning materials**
* [A Beginner’s Guide to Wireframing](https://webdesign.tutsplus.com/articles/a-beginners-guide-to-wireframing--webdesign-7399)

**Tools**  
* [Wireframe.cc](https://wireframe.cc)


### Full visual designs
> Visual design focuses on the aesthetics of a site and its related materials by strategically implementing images, colors, fonts, and other elements.  A successful visual design does not take away from the content on the page or function.  Instead, it enhances it by engaging users and helping to build trust and interest in the brand.

**Learning materials**
* [Visual Design Basics](https://www.usability.gov/what-and-why/visual-design.html)
  * A very gentle introduction into web design.
* [Web Style Guide](https://www.webstyleguide.com/wsg3/7-page-design/3-visual-design.html)
* [Bright Colors in UI Design: Benefits and Drawbacks](https://uxplanet.org/bright-colors-in-ui-design-benefits-and-drawbacks-433680f0a1c7)
* [Understanding Visual Hierarchy in Web Design](https://webdesign.tutsplus.com/articles/understanding-visual-hierarchy-in-web-design--webdesign-84)


**Tools**  
* [Krita](https://krita.org/en/download/krita-desktop)


### Navigation map
> Creating an effective website navigation system is a crucial part of ensuring usability, and the success of a web design. Good navigation should be intuitive, easy to use and most importantly help your visitors find the content they’re looking for quickly, without fuss.

**Examples**  
* [Colour-coded Navigation map](https://jasminjohnwebauthoring.files.wordpress.com/2012/11/site-map-screenshot.png)
* [Website Design Navigation map](https://creately.com/diagram/example/g35fln5c1/Website+Design)
* [Personal Page Navigation map](https://creately.com/diagram/example/go438cyo3/Personal+Page+Sitemap)
* [22 great examples of website navigation](https://www.creativebloq.com/web-design/website-navigation-4132549)


### Flowcharts
> A flowchart is a type of diagram that represents an algorithm, workflow or process. The flowchart shows the steps as boxes of various kinds, and their order by connecting the boxes with arrows. This diagrammatic representation illustrates a solution model to a given problem. Flowcharts are used in analyzing, designing, documenting or managing a process or program in various fields.

![Lamp flowchart](https://upload.wikimedia.org/wikipedia/commons/thumb/9/91/LampFlowchart.svg/220px-LampFlowchart.svg.png)

**Learning materials**  
* [Ultimate Flowchart Guide ( Complete Flowchart Tutorial with Examples )](https://creately.com/blog/diagrams/flowchart-guide-flowchart-tutorial/)
  * An excellent, comprehensive guide to flowcharts.

**Tools**  
* [Draw.io](https://www.draw.io/)


## Requirements

### Functional requirements
Functional requirements describe what the software/website should do (the functions). In other words: what user should be able to do with the website.  

### Non functional requirements
Non-functional requirements are not concerned with the functions of the system. Instead, they look at the criteria to which the software or website is expected to conform to. Non-functional requirements can include things like response time and reliability. They tend also to be closely tied to user satisfaction.   

### Examples of functional requirements of a web app
*	Accept customer orders
*	Take customer feedback
*	App must be able to produce reports (yearly, monthly, weekly)
*	Users must be able to view all products available in the shop
*	Allow adding items to basket

### Examples of non functional requirements of a web app
*	Must be intuitive and easy to use by all employees (incl. managers & other stakeholders)
*	Available in several languages (English, French, Spanish)
*	Allows to make several sales at the same time without lowering the performance of the app
*	App must be reliable (i.e. available 24/7, not crashing, etc.)
*	Must be completed/developed by a certain date
*	The initial page of the web app must load in 1s (or quicker) on desktops and 3s (or quicker) on 3G mobiles


## Types of testing

### Alpha testing 
Done internally by developers before beta version is available. Often buggy, with briefly laid down functionalities, can be rough graphic design-wise.

### Beta testing
Beta version tested by external testers. This is still a pre-release version of software.

### White box testing
Testing a web site/app knowing and understanding the code (the internal logic). Test cases always built around specific functions of the system itself. Automated unit tests (pieces of test code running against the application code) are part of white box testing.

### Black box testing 
Testing a web site/app not knowing and understanding the code. Test cases always built around functionalities of the system. Always done by a human being.

### Black box vs white box testing 
A very good, visual, explanation: https://www.quora.com/What-is-the-difference-between-black-box-testing-and-white-box-testing

### Usability testing 
Usability testing is a way to see how easy to use something is by testing it with real users. Users are asked to complete tasks, typically while they are being observed by a researcher, to see where they encounter problems and experience confusion. If more people encounter similar problems, recommendations will be made to overcome these usability issues.

### Automated unit testing 
In computer programming, unit testing is a software testing method by which individual units of source code, sets of one or more computer program modules together with associated control data, usage procedures, and operating procedures, are tested to determine whether they are fit for use.  
more on wiki: https://en.wikipedia.org/wiki/Unit_testing


## Unified Modeling Language

Unified Modeling Language (UML).  

### UML
https://en.wikipedia.org/wiki/Unified_Modeling_Language

### UML types of diagrams
https://www.smartdraw.com/uml-diagram/#UMLTypes
