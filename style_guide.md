# Style guide

Use this style guide for all JS code you write.

## Variables

Use camelcase, rather than snakecase, when naming variables. There's nothing wrong with camelcases, it's an aesthetic choice.
```
// bad
var camel_carries_water = true;

// good
var camelCarriesWater = true;
```

Every variable on a separate line.
```
// bad
var camelCarriesWater = true, maxCamelsInCaravan = 44;

// good
var camelCarriesWater = true;
var maxCamelsInCaravan = 44;
```

## Meaningful names

Always try to name your variables and functions using meaningful names. It takes some practice, and sometimes you won't get them right the first time around, but keeping your code as human-readable as possible ensures that it gets less messy as the codebase grows.

```
// bad
var students = [stud1, stud2];
var changedStudents = sortStudents(students);  // sortStudents() function does some kind of sorting

// good
var students = [student1, student2];
var sortedStudents = sortStudents(students);
```

In the example above, `student1` is more meaningful than `stud1`, and `sortedStudents` variable tells us more than `changedStudents`.

## Functions

Always start every word of function's with a capital letter
```
// bad
function show_me() {}
function showMe() {}

// good
function ShowMe() {}
```

Curly brackets always on the same line as `function` keyword.
```
// bad
function ShowMe()
{

}

// good
function ShowMe() {

}
```

No space between the function's name and the list of arguments (`()`).
```
// bad
function ShowMe (argument) {}

// good
function ShowMe(argument) {}
```

Space between list of arguments the and opening curly bracket (`{`).
```
// bad
function ShowMe(argument){}

// good
function ShowMe(argument) {}
```

As a general rule, always break things into functions. It increases maintainability.
```
// bad
var humans = [human1, human2, human3];
var newHumans = [];

for (var i=0; i < humans.length; i++) {
  var newHuman = humans[i].name;
  newHumans.push(newHuman);
}

// good
var humans = [human1, human2, human3];
getHumansNames(humans); // calls the getHumansNames function

function getHumansNames(humans) {
  var newHumans = [];

  for (var i=0; i < humans.length; i++) {
    var newHuman = humans[i].name;
    newHumans.push(newHuman);
  }
}
```


## Arrow functions

Arrow functions were introduced with JavaScript version 6 (2015) to let coders write shorter code.  
You will find them used all over examples and tutorials on server-side JavaScript (i.e. NodeJS, Express).  
That's what they look like in a typical Express app:
```
app.get('/', (req, res) => {
  res.send('Hello World!')
})
```

Using older JS syntax, we could write it like so:
```
app.get('/', function (req, res) {
  res.send('Hello World!')
})
```

In other words:
```
// this
(req, res) => {}

// equals this
function(req, res) {}
```

Because the two differ not just on the aesthetic grounds, use arrow functions only when you know what you're doing to avoid unexpected errors.  
Read more about them (and how they differ from the old syntax) on MDN: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions


## Conditionals

Break conditions nicely into lines.   
Closing curly bracket on the same line as `else if` and `else` keywords.  
Conditional code in its own line(s).
```
// bad
if (true) { return true; } else if (false) { return false; } else {}

// good
if (true) {
  return true;
} else if (false) {
  return false;
} else {

}
```

Always use `else` keyword. It increases readability.
```
// bad
var camelsReturned = 22;
if (camelsReturned > 10) {
  return "Success!";
}
return "Fail...";

// good
var camelsReturned = 22;
if (camelsReturned > 10) {
  return "Success!";
} else {
  return "Fail...";
}
```

Avoid ternary operator (`condition ? true : false`).
```
// bad
var camelsReturned = 22;
camelsReturned > 10 ? "Success!" : "Fail...";  // ternary operator

// good
var camelsReturned = 22;
if (camelsReturned > 10) {
  return "Success!";
} else {
  return "Fail...";
}
```

## Semi-colons

Always apply semi-colons.
```
// bad
var camelsReturned = 22
function () {
  return true
}; // this is wrong because function's don't need semi-colons at the end

// good
var camelsReturned = 22;
function () {
  return true;
}
```

## Indentation

Indentation (or whitespace) increases readability.  
Modern code editors (like Atom) allow to set a specific size of a tab (e.g. 2 spaces). Using tabs over spaces (or the other way around) has been a subject of many quarrels between coders; Atom has an option to turn all tabs into spaces, allowing you to use any. The benefit of spaces is that your code will look the same on every computer, in every environment (tabs produce different results).  
In Atom, `Ctrl+[` and `Ctrl+]` are shortcuts for moving lines one tab left and right (outdent and indent).
```
// bad
function MyFunction() {
for (var i=0; i < 5; i++) {
console.log(i);
}
}

// good
function MyFunction() {
  for (var i=0; i < 5; i++) {
    console.log(i);
  }
}
```

## Objects

Object's properties should be on separate lines.  
Property's key (e.g. `a`) should be followed by `:` and a space. Only then should it be followed by a value (e.g. `1`).
```
// bad
var obj = {a:1,b:2};

// good
var obj = {
  a: 1,
  b: 2
};
```

You might sometime call a key a more complex name. Use camelcase.
```
// bad
var obj = {
  'low-score': 1,
  'high-score': 1
};

// good
var obj = {
  lowScore: 1,
  highScore: 1
};
```

## Arrays

Space-separated elements.
```
// bad
var initialArray = [1,2,3];

// good
var initialArray = [1, 2, 3];
```

Array of objects not clumped in one line.

```
// bad
var initialArray = [{id: 1, name: 'J'}, {id: 2, name: 'D'}, {id: 3, name: 'L'}];

// good
var initialArray = [
  {
    id: 1,
    name: 'J',
  },
  {
    id: 2,
    name: 'D',
  },
  {
    id: 3,
    name: 'L',
  },
];
```

## Working with arrays [advanced]

Use `map` over `for` loop, if you can. `map` is declarative, thus easier to express and quicker to write.  
Underneath the hood, `Array.prototype.map` uses a `for` loop.
```
// bad
var initialArray = [1, 2, 3];
var newArray = [];

for (var i=0; i < initialArray.length; i++) {
  newArray.push(initialArray[i] * 2);  // => 2, 4, 6
}

// good
var initialArray = [1, 2, 3];
var newArray = initialArray.map(function(number) { return number * 2; });  // => 2, 4, 6
```

Additional benefit of `map` is our ability to name the anonymous function that `map` takes as its argument.
```
// not bad, but could be nicer
var initialArray = [1, 2, 3];

var newArray = initialArray.map(function(number) { return number * 2; });

// better
var initialArray = [1, 2, 3];

var newArray = initialArray.map(TimesTwo);

function TimesTwo(number) {
  return number * 2;
}
```

## Event listeners

The old syntax for having an element that does something on a specific event (e.g. click) looks like this:  
```
<button onclick="Action()">Action!</button>

function Action() { ... }
```

The newer (and sometimes preferred) syntax looks differently:
```
<button id="Button">Action!</button>

var btn = document.getElementById('Button');

btn.addEventListener(function(event) {
  Action();
});

function Action() { ... }
```

As you can see, the second version requires more code, but comes with one advantage: separation of concerns. What it means is that all our logic lives in JavaScript, while HTML has no JavaScript at all, it is merely a document. Separation of concerns is one of big ideas in web dev, but many popular solutions do not subscribe to it. In the end, it will be your choice whether you prefer `onclick="..."` syntax, or `addEventListener(function(event) {...})`.  
Ask your lecturer if you would like to discuss it in more detail.  

More on separation of concerns: https://en.wikipedia.org/wiki/Separation_of_concerns


## Namespace [advanced]

Read the web, you might come across a phrase "do not polute the namespace". Namespace, in JavaScript, is the topmost level of variables. If you simply declare a global variable in your code, e.g. `var myVariable = true;`, you will be able to access it in your browser's console by typing `myVariable`.  
The problem here is that you might load some library that uses the very same name of the variable, overwrite it, and get errors difficult to understand. There's a simple solution to this (as a precaution).

```
// bad
var myVar = true;
var myOtherVar = false;

// good
var myNamespace = {};
myNamespace.myVar = true;
myNamespace.myOtherVar = false;
```

Now all variables are properties of just one object literal referenced by variable `myNamespace`, and to access a variable you will need to type `myNamespace.myVar`.  
To save yourself typing, coders often just use an abbreviation of a project's name. So, let's say my project is called LeaderBoards. Abbreviation would be `LB`.

```
// good
var LB = {};
LB.myVar = true;
LB.myOtherVar = false;
```
