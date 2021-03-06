# Node.js + Express + Codeanywhere tutorials

## Table of contents

* [What is Node?](#what-is-node)
* [Should I use plain Node?](#should-i-use-plain-node)
* [Why Express?](#why-express)
* [What is API?](#what-is-api)
* [Codeanywhere.com](#codeanywhere)
* [Codeanywhere. Step 1: Sign up](#codeanywhere-step-1-sign-up)
* [Codeanywhere. Step 2: Create the app](#codeanywhere-step-2-create-the-app)
* [Codeanywhere. Step 3: Familiarize yourself with the app](#codeanywhere-step-3-familiarize-yourself-with-the-app)
* [Codeanywhere. Step 4: Initialise new Node project and install Express](#codeanywhere-step-4-initialise-new-node-project-and-install-express)
* [Codeanywhere. Step 5: Working web server and Hello World](#codeanywhere-step-5-working-web-server-and-hello-world)
* [Create your first route and employ a Nodemon daemon](#create-your-first-route-and-employ-a-nodemon-daemon)
* [Have our route respond with HTML file](#have-our-route-respond-with-html-file)
* [Simpler way to respond with HTML file](#simpler-way-to-respond-with-html-file)
* [What about static files such as CSS and client side JS](#what-about-static-files-such-as-css-and-client-side-js)
* [How about passing some dynamic data to an HTML template](#how-about-passing-some-dynamic-data-to-an-html-template)
* [Sessions](#sessions)
  * [Initiating session middleware](#initiating-session-middleware)
  * [Accessing the session object](#accessing-the-session-object)
  * [Modifying the session object](#modifying-the-session-object)
* [Body parsing aka parsing web forms data](#body-parsing-aka-parsing-web-forms-data)
  * [Web forms](#web-forms)
  * [Parsing data on the server](#parsing-data-on-the-server)
    * [Setup](#setup)
    * [Usage](#usage)



## What is Node

https://www.w3schools.com/nodejs/nodejs_intro.asp

## Should I use plain Node

No, we will be using a low-level framework called Express. https://expressjs.com/

## Why Express

Node is low-level. More low-level than Express :) Express is an abstraction layer, a framework created by coders for coders that exposes a set of useful, more human-readable functions (or API) that make developing in server-side JS a much easier task than using plain Node's API.

## What is API

API means `Application Programming Interface`. Simply put: it's a set of functions that wraps some code and are exposed for other coders to use. API is always created to simplify things for other coders. The word API is usually used in the context of systems that allow you to interact with them (e.g. Paypal API, Instragram API, Stripe API). But what frameworks do (server- or front-side) is really API as well. And test frameworks do the same, e.g. using QUnit you will also find that it has an API (a set of functions that you can use within the QUnit testing framework). A driver to interact with MySQL database also exposes an API. And so on.

## Codeanywhere

Codeanywhere allows you to code from whenever you want. (Provided that you choose a Node.js project at the beginning) It comes with Node, npm, MySQL, and a few other useful things installed. It also runs on an Ubuntu (Linux) operating system.

## Codeanywhere Step 1 Sign up

1 Go to: https://codeanywhere.com  
2 Sign up.  
3 Go to Editor.

## Codeanywhere Step 2 Create the app

1 Create a new project.  
2 File > New Project > (here enter the name of your project, e.g. `MyFirstApp`)  
3 In the modal that just popped up enter the name of the project (e.g. `MyFirstApp`)  
4 In the list of tech stacks find `Node.js` matched with `Ubuntu`.  
5 Scroll down the screen and click on `CREATE` button.  
6 Wait until `Deploying container` disappears.

## Codeanywhere Step 3 Familiarize yourself with the app

You should now see two opened tabs, each called by the name of your project. The first one is a console (or terminal). That's a way to interact with Ubuntu OS directly.  
The second one is an info file telling you more about your project. Read it twice. Familiarize yourself with it. Leave it open. You will be coming back to it in the future.

## Codeanywhere Step 4 Initialise new Node project and install Express

1 Go to terminal (1st tab, or (left hand side) right click on the name of your project under `Connections` and choose `SSH Terminal`).  
2 Type `npm init` and hit enter. This will initialise a new Node.js project. You will be asked several questions. Just hit enter to accept the default values for each question.  
3 Now type `ls` (a command to list files in the directory). You should see only one file: `package.json`.  
4 Reload the browser's tab. The browser will likely ask about leaving the page. Confirm 'Leave'. (This will show `package.json` correctly in the list of files on the left hand side.)  
5 Now you should see `package.json` showing properly.  
6 Go back to the console (terminal), and type `npm install express --save`. This will install the Express framework + save it as a dependency in `package.json` file.  
7 Open your `package.json` file. You should see a line that looks something like this: `"express": "^4.16.4"` (note that the exact version of express will likely be a bit different).  

## Codeanywhere Step 5 Working web server and Hello World

Let's now create the most basic web server using Express framework.  
1 Create an `index.js` file.  Alt+N (to Create New File...) > Ctrl+S (to Save it) > Name it `index.js` > Click on the name of your project to create a connection.  
2 Visit this page: https://expressjs.com/en/starter/hello-world.html  
3 Copy/paste the code from it (6 lines of code).  
4 Save `index.js` file (Ctrl+S).  
5 Go to terminal tab.  
6 Type `node index.js`.  
7 You should see `Example app listening on port 3000!` in the terminal.  
8 Go to the info tab (2nd tab by default OR right click on the name of your project under `Connections` (left hand side) and choose `Info`).  
9 In the opened Info tab, scroll down, and click on the first link. It starts with `http(s)`.  
10 In the newly opened tab, you should see `Hello World!`.  
11 Congrats!! Your first app is running smoothly on a remote server, somewhere in the world :-)


## Create your first route and employ a Nodemon daemon

Routes are server's API. They specify what happens when someone (or something) accesses a specific url (e.g. http://example.com/about). In this case `/about` is a route. It has to respond with something, otherwise user will see an error message ([404](https://en.wikipedia.org/wiki/HTTP_404)).  

1 Go to your `index.js` file.  
2 Copy L5 (line 5).  
3 Paste it underneath L5 (it will become your new L6).  
4 Change `'/'` to `/about`. And `'Hello World!'` to `About route!`.  
5 Now, in your other tab where your app is accessed/opened, at the end of the url type `/about`. You should see `Cannot GET /about`. Not exactly what we want, right? Easy fix! Go to terminal tab, stop the server (`Ctrl+C`), and push the `up-arrow` on your keyboard to bring `node index.js` again (just a little time-saving trick).  
6 Go back to the tab with your app and reload the page. You should now the about page shouting `About route!`. Awesome!!  
7 But that's a bit tiring, to have to always restart your web server manually. Let's automate it!  
8 In your terminal, stop the server (`Ctrl+C`).  
9 Now type: `npm install nodemon --save-dev`. It will install a npm (Node Package Manager) package called nodemon -- a daemon to keep our server running and re-running on any changes. Cool, huh? :-)  
10 Once installed, we need to edit `package.json` file. Underneath L6 (that reads: `"scripts": {`) we need to add a new line: `"start": "nodemon index.js",`. This will make sure that on typing `npm start` nodemon gets executed. Npm allows us to create scripts like that. It's pretty useful.  
11 Now, back in terminal, type `npm start`. This will launch the script we've created in `package.json`. Cool! Awesome!! From now on, always start your project with `npm start`.  
12 Great!! You've just created a new route that responds with a simple string when someone/thing accesses it! And you've made your server to "automagically" reload on any change you make to files -- fantastic!


## Have our route respond with HTML file

So far our routes have been responding with simple strings. That's useful to test things out, but that's not what we expect from our web site. We expect it to send HTML. Let's see how we can accomplish that.  

1 We could try to tell Express how to load static HTML files from the server, but that's not very future-thinking. Instead, let's make 1 step further, and invest into a `templating engine`. There's many, but we're going to use one called `Nunjucks` created and used by Mozilla (company behind Firefox). `Nunjucks` is heavily inspired by `jinja2` -- a templating engine used in Python. Funny story, Mozilla uses a lot of Python, but writes new code in Node.js.  
2 For references and future use. Nunjucks site: https://mozilla.github.io/nunjucks/  
3 Go to the terminal tab. Type: `npm install nunjucks --save`.  
4 Now, let's enable `nunjucks` in Express.  
5 In `index.js` add these lines right after L2:
```
const nunjucks  = require('nunjucks');

nunjucks.configure('views', {
  autoescape: true,
  express   : app
});
```
6 Great. This enables `nunjucks` in our app AND points it to `views` folder where our files should live. We don't have `views` folder yet, so let's create it.  
7 Right click on the name of your project underneath `Connections` and click on `Create Folder`. Name it `views`.  
8 Let's create our first HTML file: `about.html`. Right click on the newly created `views` folder, choose `Create File`, and name it `about.html`.  
9 Add this code to `about.html`: `<h1>About route!</h1>`, and save it.  
10 Great. Let's get back to `index.js` to actually render the file when `/about` route is accessed.  
11 L11 currently reads: `app.get('/about', (req, res) => res.send('About route!'));`. Let's change the `res.send('About route!')` bit to `res.render('about.html')`.  
12 Switch to the app tab, make sure the url ends with `/about`, reload the page, and you should see big header saying `About route!`.  
13 Congrats! Your first HTML file sent from the server to your browser, rendering HTML!!

## Simpler way to respond with HTML file

Nunjucks is great when you want to pass some dynamic data from the database (or just some static data you keep in a .js file on the server), but when your App is mainly client-side App, there's a decent chance all you will need is just to send an .html file using `sendFile()`. Here's how you can do that using `/example` route as an example:  

```
...

app.use(express.static('static'))

app.get('/example', (req, res) => {
  res.sendFile('example.html');
});

...
```

Simply put, we are serving `example.html` as a static asset. Check the next chapter to learn about serving static files/assets.

## What about static files such as CSS and client side JS

Good question! We need our web server to serve static files (such as CSS and client/browser-side JS). Let's tell our app what folder it should treat as a source of 'static' files. Express makes it pretty easy for us.  
Reference: https://expressjs.com/en/starter/static-files.html  

1 At the top level of your project, create a new folder called `static`.  
2 In `index.js`, between L3 and L5, add a new line of code: `app.use(express.static('static'))`. Your code should now look like this:
```
...
const nunjucks  = require('nunjucks')

app.use(express.static('static'))  // <= this is the new line

nunjucks.configure('views', {
  autoescape: true,
  express   : app
});
...
```
3 Save the file.  
4 Create a new folder inside `/static`. Call it `js`. You will keep your client-side JS files there.  
5 Inside `/static/js` create a new JS file called `app.js`.  
6 In your `/static/js/app.js` add a simple line of code: `console.log('App!');`.  
7 To test if the web server exposes static files properly, go to your browser, switch to the tab where you're accessing your app, and add this to the end of the url: `/js/app.js`. It should display `console.log('App!');` on the screen.  
8 Great! That's static files for us!


## How about passing some dynamic data to an HTML template

Let's say we have some comic books stored in our MySQL database. Let's furthermore say that we've just started modelling our data, and every comic book is pretty barren, and only has an `id` and a `title`.

```
app.get('/comics', (req, res) => {
  var comics = [
    {id: 1, title: 'V for Vendetta'},
    {id: 2, title: 'Incal'},
  ]  // this is just dummy data, you would normally fetch them from MySQL

  res.render('comics.html', {comics: comics});
});
```

Notice that `res.render` now takes two arguments (a string: name of HTML template that needs to be present in `views` folder, and an object literal: `{comics: comics}` (the first `comics` is the name of the property (or key), the second is the value (in this case, our array of comics stored in `comics` variable))).  

Then, we need to create `comics.html` in `views` folder, and make it look like this:
```
<h1>Comics</h1>
<ul>
{% for comic in comics %}
  <li>{{ comic.title }}</li>
{% else %}
  <li>This would display if the 'comics' array was empty</li>
{% endfor %}
</ul>
```

The above uses Nunjucks to dynamically create some HTML content. Here, we use `for` loop to loop over every `comic` in `comics` array. Then, inside this loop, we can access properties of every single comic, e.g. `comic.title`.  
Try displaying the `id` of every comic. [hint: `comic.id`].


## Sessions

HTTP requests (usually sent by the browser) are stateless, meaning that accessing `example.com/` and `example.com/about` from the same browser (to the server) counts as two independent connections.  
From our point of view, though, that's just one user. And, often, we need to be able to keep the state of the user (typical example would include: `isUserAuthenticated` `==` `true`/`false`). For that reason, we need to store a session for each user.  

By now you should know how to install npm (Node Package Manager) packages. For our needs, we will be using [express-session](https://www.npmjs.com/package/express-session) package.  
What this package does, in a nutshell, is:  
1. Stores session data in a chosen storage on the server (`MemoryStore` by default, meaning: it stores data in memory).
2. Creates cookie on the client with a Session ID only.

### Initiating session middleware

Before we start, `middleware` is a piece of code that fires after a request hits the server, but before a requested route's code is actually accessed.  
Now, this is what you need to initiate a session:
```
var app = express();
var session = require('express-session');
var sessionOptions = {
  secret: '0f9sdui09fusd0uau40ru4ekc;klsdkz;lzs[2oe340#d]',  // session's secret (make sure to type a different string of random characters here)
  resave: false,
  saveUninitialized: false,
  cookie: { secure: false }
};

// the code below allows you to get secure cookies in production
// but non-secure cookies in development
// secure cookies would crush your app in development, hence
// we use a conditional here
if (app.get('env') === 'production') {
  app.set('trust proxy', 1); // trust first proxy
  sessionOptions.cookie.secure = true; // serve secure cookies
}

app.use(session(sessionOptions));
```

And that's it. That's your session initialized and silently doing it's thing!

### Accessing the session object

This is pretty simple. Inside a route's callback function (where `req` and `res` objects are available), you can do this:
```
req.session;
```

And because `req.session` is an object, you can dig deeper into it, like so:
```
req.session.username;  // if no 'username' was saved prior to accessing it, you will get 'undefined'
```

### Modifying the session object

Again, it's pretty basic JavaScript. You can modify a property or add it to `req.session` object like so:
```
req.session.username = "Gregory McPeanut";
req.session.age = 33;
req.session.loggedIn = true;
```

Then, you can access the session data easily:

```
req.session.username; // => "Gregory McPeanut"
req.session.age // => 33
req.session.loggedIn // => true
```

If you need help understanding sessions, let your Lecturer know. But before you do this, check out this [explanation](https://stackoverflow.com/questions/3804209/what-are-sessions-how-do-they-work#3804387), it's pretty decent :)



## Body parsing aka parsing web forms data

### Web forms

Web forms are ways of sending data from the browser to the server.  
Forms have various input types, such as `text`, `radio`, `checkbox`, `textarea`.  

As a matter of fact, you have been filling in forms a lot on the web. Whenever you sign up or log in, you fill up a form. If you change your settings on a site, you fill up a form. When you take a survey, or simply write a new post or a comment. It's all forms.  

At the simplest, the form consists of `<form></form>` tag, at least one `<input>` tag and a `<button type='submit'></button>` tag.  

Look at this example:  
```
  <form method='POST' action='/name'>
    <input type='text' name='name' placeholder='What's your name, amigo/a?'>
    <button type='submit'>send</button>
  </form>
```
1. `<form>` comes with two attributes:
    * `method`, which is almost always `POST` because we will be "posting" data to the server
    * `action`, which is the route we will be targetting on the server
1. `<input>` field comes with many attributes, but these are the core ones:
    * `type`, which is usually `text`, but can also be `radio` or `checkbox` (try them out to see what they do)
    * `name`, which will become a property of `req.body` object on the server (e.g. if we have `name='name'`, we will be able to access user's input using `req.body.name` (don't worry if you don't get it now, the next chapter explains it in detail).
    * `placeholder`, which is a helpful way to let the user understand what we want them to type.
1. `<button>` comes with just one attribute:
    * `type='submit'`, which tells the form that when the button is clicked, the form should be send to the route specificed in `<form>`'s `action` attribute.
    
That's all you need to submit a form to the server.  

Read more about forms: https://www.w3schools.com/html/html_forms.asp

### Parsing data on the server

#### Setup

To parse data from web forms on the server, we need to add `body-parser` module to our application.

1. Open the SSH Terminal/Console.
1. Make sure you are in the root folder of your app.
1. Install the module: `npm install --save body-parser`.
1. In your `index.js` file add these lines of code:
```
const bodyParser = require('body-parser');

// parse application/x-www-form-urlencoded
app.use(bodyParser.urlencoded({ extended: false }));
```
Make sure that your code for routes is below these lines.  

Now you are all set up and ready to go.  

#### Usage

Let's use the super simple form from before. It has just one `input` field, `name`.  
The form (using `action` attribute) hits a `POST` route on the server, `/name`.  

Let's grab the data on the server.  

First, create a `POST` route, like so:
```
app.post('/test', (req, res) => {

})
```

Then, access the data sent from the browser using `req.body`.
```
app.post('/test', (req, res) => {
  console.log(req.body)       // req.body is where all the data sent from the browser live
  console.log(req.body.name)  // req.body.name will give us the value sent from the browser (it will of type String)
                              // so if the user typed "John", we will get a string "John"
})
```

Respond with something meaningful. At minimum we want to give the user a confirmation that the data was received successfully.
```
app.post('/test', (req, res) => {
  console.log(req.body)       // req.body is where all data sent from the browser live
  console.log(req.body.name)  // req.body.name will give us the value sent from the browser (it will of type String)
                              // so if the user typed "John", we will get a string "John"
  res.send("We have received your name successfully. Thanks.")
})
```

In reality, we would rather show the user some sort of a nice confirmation page (using `res.render()`, rather than `res.send()`), but for the purpose of this tutorial, the above is enough.
