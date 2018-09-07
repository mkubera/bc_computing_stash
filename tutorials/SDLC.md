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
  * [UML diagrams](#uml-diagrams)

## Software Development LifeCycle

In a nutshell, **SDLC** involves:  

1.	**Planning** (Analysis)
    *	Functional requirements
    *	Non-functional requirements
2.	**Design**
    *	Wireframes
    *	Full designs
    * Navigation map
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
more on Agile: https://en.wikipedia.org/wiki/Agile_software_development  
A good example of an Agile approach that suits small-scale applications is SCRUM.  
more on SCRUM: https://en.wikipedia.org/wiki/Scrum_(software_development)  

### Waterfall
**Waterfall** is the old way of doing things, it’s still in use, but is falling out of fashion as it’s too slow to respond to software’s changing requirements.  
Simply put, it is called waterfall because it goes step by step (Planning, Designing, Developing, Testing) from top to bottom, but it never goes back in the process; meaning, if there’s a fault in Planning, but the team is already on Developing stage, waterfall doesn’t provide flexibility to go back to Planning, and fix things.  
As you can see, given the example above, waterfall is a crippled model for software development. Shortcomings of **Waterfall** prompted development teams to look for different solutions. **Agile** is a great example of one as it allows iterating over an App repeatedly.  
more on Waterfall: https://en.wikipedia.org/wiki/Waterfall_model  

### Spiral
**Spiral** is just Waterfall but repeated over and over again.  
more on Spiral: https://en.wikipedia.org/wiki/Spiral_model  

### Further reading
Read more about all three models here: https://apprenticeoscar.wordpress.com/2018/02/23/sequential-iterative-and-incremental/   
Read about Waterfall vs Spiral models of systems development + (dis)advantages here: https://techspirited.com/comparison-between-waterfall-model-spiral-model  


## Prototype revolutionary vs evolutionary

### Revolutionary prototyping
> "Revolutionary, pr "Throwaway", prototyping is where the objective of the evolutionary development process is to understand the customer's requirements and hence develop a better requirements definition for the system. The prototype concentrates on experimenting with the customer requirements that are poorly understood."

### Evolutionary prototyping
> "Exploratory development where the objective of the process is to work with the customer to explore their requirements and deliver a final system. The development starts with the parts of the system that are understood. The system evolves by adding new features proposed by the customer."  


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

### UML diagrams
https://en.wikipedia.org/wiki/Unified_Modeling_Language#Diagrams
