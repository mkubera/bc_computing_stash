# JS Form Validation TUTORIAL

## Setup

For the simplicity's sake, we will have all our JS code inside the .html file in this tutorial (normally, you would use a linked .js file).  

First, start with the basic HTML structure:  

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>JS tutorial</title>
</head>
<body>

  <div id="Wrapper">



  </div>
  
  <script>
    
  </script>
</body>
</html>
```

Notice that all we have in our `<body` tag is a `<div>` with `id` `Wrapper` for all our HTML code and a `<script>` tag for all our JS code.


## Create a form with input fields and a submit button

Insert the code below between the `<div id="Wrapper">` and `</div>` tags.

```
  <form>

      <input id="InputUsername" type="text" placeholder="username"><br>
      <input id="InputGenderM" type="radio" name="gender"> Male
      <input id="InputGenderF" type="radio" name="gender"> Female <br>
      <input id="InputTandC" type="checkbox"> I agree to the Terms and Conditions <br>
      <input id="InputSubmit" type="submit" value="submit">
      
  </form>
```

So now we have the HTML code with our Form ready. The form has 1 text input, 1 checkbox input, 2 radio inputs ("linked" together via `name="gender"` attribute), and a submit button (technically, also an input).

## JS: add an Event Listener to the submit button

Inside the `<script>` tag add:

```
    var submitButton = document.querySelector('#SubmitButton'); // targets the submit button

    submitButton.addEventListener('click', function(event) {
      event.preventDefault(); // prevents the form from being sent to the server
                             // (keeps it client/browser-side and prevents
                             // the browser from awkward reloading)

      
    })
```

The code above will target the submit button in the form, attach an Event Listener to it that will listen on a click event, 
so that when user clicks the button, we can run some code.

## JS: gather user input from <input> tags

We are now going to gather user's input from all the `<input>` tags, step by step, like so:

### Gather input from text field

First, we need to target the text input (the one that takes in user's username).  

```
var inputUsername = document.querySelector('#InputUsername'); // targets the username input
```

Second, let's gather the value of the text input, so that we know what user actually typed.

```
var username = inputUsername.value;
```

Your JS code should now look like this:
```
    var submitButton = document.querySelector('#SubmitButton'); // targets the submit button
    var inputUsername = document.querySelector('#InputUsername'); // targets the username input

    submitButton.addEventListener('click', function(event) {
      event.preventDefault(); // prevents the form from being sent to the server
                             // (keeps it client/browser-side and prevents
                             // the browser from awkward reloading)

      var username = inputUsername.value; // the value will be a String
      
    })
```

### Gather input from radio buttons

Now, we want to know if user chose any of the radio buttons.

First, we need to target the radio inputs:
```
    var inputGenderM = document.querySelector('#InputGenderM'); // targets the male gender input
    var inputGenderF = document.querySelector('#InputGenderF'); // targets the female gender input
```

Second, we need to find out whether they are checked or not, which will be a Boolean value (`true` or `false`).

```
      var genderM = inputGenderM.checked; // the value will be a Boolean
      var genderF = inputGenderF.checked; // the value will be a Boolean
```

Your code should now look like this:

```
    var submitButton = document.querySelector('#SubmitButton'); // targets the submit button
    var inputUsername = document.querySelector('#InputUsername'); // targets the username input
    var inputGenderM = document.querySelector('#InputGenderM'); // targets the male gender input
    var inputGenderF = document.querySelector('#InputGenderF'); // targets the female gender input

    submitButton.addEventListener('click', function(event) {
      event.preventDefault(); // prevents the form from being sent to the server
                             // (keeps it client/browser-side and prevents
                             // the browser from awkward reloading)

      var username = inputUsername.value; // the value will be a String
      var genderM = inputGenderM.checked; // the value will be a Boolean
      var genderF = inputGenderF.checked; // the value will be a Boolean

    })
```

### Gather input from checkbox

Checkboxes and radio buttons, when it comes to gathering feedback, are the same.  

First, let's target the checkbox input, though:
```
var inputTandC = document.querySelector('#InputTandC'); // targets the TandC input
```

Second, let's gather user's input:
```
var tandc = inputTandC.checked; // the value will be a Boolean
```

Your code should now look like this:

```
    var submitButton = document.querySelector('#SubmitButton'); // targets the submit button
    var inputUsername = document.querySelector('#InputUsername'); // targets the username input
    var inputGenderM = document.querySelector('#InputGenderM'); // targets the male gender input
    var inputGenderF = document.querySelector('#InputGenderF'); // targets the female gender input
    var inputTandC = document.querySelector('#InputTandC'); // targets the TandC input

    submitButton.addEventListener('click', function(event) {
      event.preventDefault(); // prevents the form from being sent to the server
                             // (keeps it client/browser-side and prevents
                             // the browser from awkward reloading)

      var username = inputUsername.value; // the value will be a String
      var genderM = inputGenderM.checked; // the value will be a Boolean
      var genderF = inputGenderF.checked; // the value will be a Boolean
      var tandc = inputTandC.checked; // the value will be a Boolean
    })
```

### JS: console.log all inputs

To check if the code is fine, let's console.log all inputs to see what we are getting.  

We'll use an array to log all the variables inside the `addEventListener` function, like so:

```
console.log([username, genderM, genderF, tandc]);
```

Your code should now look like this:
```
    var submitButton = document.querySelector('#SubmitButton'); // targets the submit button
    var inputUsername = document.querySelector('#InputUsername'); // targets the username input
    var inputGenderM = document.querySelector('#InputGenderM'); // targets the male gender input
    var inputGenderF = document.querySelector('#InputGenderF'); // targets the female gender input
    var inputTandC = document.querySelector('#InputTandC'); // targets the TandC input

    submitButton.addEventListener('click', function(event) {
      event.preventDefault(); // prevents the form from being sent to the server
                             // (keeps it client/browser-side and prevents
                             // the browser from awkward reloading)

      var username = inputUsername.value; // the value will be a String
      var genderM = inputGenderM.checked; // the value will be a Boolean
      var genderF = inputGenderF.checked; // the value will be a Boolean
      var tandc = inputTandC.checked; // the value will be a Boolean

      console.log([username, genderM, genderF, tandc]);
    })
```

Open your .html file in a browser, open dev tools, go to Console (or equivalent), and see if you get anything. 
If you haven't touched the form, the output should be something like this:
```
["", false, false, false]
```

Meaning that the username field is empty (`""`), and both radios and the checkbox are not checked (`false`).




