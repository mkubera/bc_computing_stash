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
      <input id="SubmitButton" type="submit" value="submit">
      
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


## JS: Validate the form

Good. We are now ready to validate the form.  

To validate the form, we need to create a condition. The condition will check if all the gathered inputs are correct. If they are not, it will say `"not valid"`. If they are, it will say `"valid"`. We will do it like so:

```
      // validation
      if (username === "" || (!genderM && !genderF) || !tandc) {
        console.log("not valid");
      } else {
        console.log("valid");
      }
```

The proper way to read it in a human language-like fashion is this:  
*If the username is empty (`username === ""`) OR neither gender male nor gender female is clicked (`(!genderM && !genderF)`) OR terms & conditions are not ticked (`!tandc`)* then log `"not valid"` into the console.  
`!` in JS reverts the Boolean value. So `!tandc` means not `true`/`false`. If `tandc` is `true`, this then becomes `!true` (not `true`). `!true` is equal to `false`.

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

      // validation
      if (username === "" || (!genderM && !genderF) || !tandc) {
        console.log("not valid");
      } else {
        console.log("valid");
      }
    })
```


## Display a nice message (error or success) to user

First, we need to ready our HTML to show either an error or a success message to user. We will achieve it by hiding and showing HTML elements. For that, we will utilise a simple CSS `.hidden` class. For simplicity's sake, we will write our CSS inside HTML (normally, you would use an external (linked) stylesheet).

First, let's create the `.hidden` class. We need to add a `<style>` tag to `<head>`, like so:

```
  <style>
    .hidden { display: none; }
  </style>
```

Your `<head>` tag should now look like this:

```
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Document</title>
  <style>
    .hidden { display: none; }
  </style>
</head>
```

Second, we need two HTML elements/tags to display error and success messages. We can use simple `<div`s for that. Let's create two of them inside `<div id="Wrapper">`.

```
    <div id="ErrorMsg" class="hidden">Error. Make sure to fill in all the fields in the form.</div>
    <div id="SuccessMsg" class="hidden">Success! Thanks for submitting your form.</div>
```

Notice how each `<div>` has the `hidden` class attached to it. This way these elements will be hidden when user first sees the form. We will be showing them conditionally using the form validation.

The `Wrapper` `<div>` should now look like that:

```
  <div id="Wrapper">

    <div id="ErrorMsg" class="hidden">Error. Make sure to fill in all the fields in the form.</div>
    <div id="SuccessMsg" class="hidden">Success! Thanks for submitting your form.</div>

    <form>

      <input id="InputUsername" type="text" placeholder="username"><br>
      <input id="InputGenderM" type="radio" name="gender"> Male
      <input id="InputGenderF" type="radio" name="gender"> Female <br>
      <input id="InputTandC" type="checkbox"> I agree to the Terms and Conditions <br>
      <input id="SubmitButton" type="submit" value="submit">

    </form>

  </div>
```

Third, we need JS to conditionally show the right message to user.  

First, let's target the message tags:

```
    var errorMsg = document.querySelector('#ErrorMsg'); // targets the error message
    var successMsg = document.querySelector('#SuccessMsg'); // targets the success message
```

Your JS code inside `<script>` tag should now look like this:

```
    var submitButton = document.querySelector('#SubmitButton'); // targets the submit button
    var inputUsername = document.querySelector('#InputUsername'); // targets the username input
    var inputGenderM = document.querySelector('#InputGenderM'); // targets the male gender input
    var inputGenderF = document.querySelector('#InputGenderF'); // targets the female gender input
    var inputTandC = document.querySelector('#InputTandC'); // targets the TandC input
    var errorMsg = document.querySelector('#ErrorMsg'); // targets the error message
    var successMsg = document.querySelector('#SuccessMsg'); // targets the success message

    submitButton.addEventListener('click', function(event) {
      event.preventDefault(); // prevents the form from being sent to the server
                             // (keeps it client/browser-side and prevents
                             // the browser from awkward reloading)

      var username = inputUsername.value; // the value will be a String
      var genderM = inputGenderM.checked; // the value will be a Boolean
      var genderF = inputGenderF.checked; // the value will be a Boolean
      var tandc = inputTandC.checked; // the value will be a Boolean

      console.log([username, genderM, genderF, tandc]);

      // validation
      if (username === "" || (!genderM && !genderF) || !tandc) {
        console.log("not valid");
      } else {
        console.log("valid");
      }
    })
```

Now, let's conditionally show/hide the messages.

```
      // validation
      if (username === "" || (!genderM && !genderF) || !tandc) {
        console.log("not valid");
        errorMsg.classList.remove('hidden');
        successMsg.classList.add('hidden');
      } else {
        console.log("valid");
        errorMsg.classList.add('hidden');
        successMsg.classList.remove('hidden');
      }
```

Every HTML tag/element has a `classList` (a list of CSS classes attached to it). We can, using JS, `add` and `remove` classes from this list. That's what we do when we `errorMsg.classList.remove(...)` and `successMsg.classList.add(...)`. If you wonder where do these properties (`classList`) and methods (`add()`, `remove()`) come from, they are part of JS Web API. Check the [element.classList](https://developer.mozilla.org/en-US/docs/Web/API/Element/classList) for more information.

The JS code should now look like this:

```
    var submitButton = document.querySelector('#SubmitButton'); // targets the submit button
    var inputUsername = document.querySelector('#InputUsername'); // targets the username input
    var inputGenderM = document.querySelector('#InputGenderM'); // targets the male gender input
    var inputGenderF = document.querySelector('#InputGenderF'); // targets the female gender input
    var inputTandC = document.querySelector('#InputTandC'); // targets the TandC input
    var errorMsg = document.querySelector('#ErrorMsg'); // targets the error message
    var successMsg = document.querySelector('#SuccessMsg'); // targets the success message

    submitButton.addEventListener('click', function(event) {
      event.preventDefault(); // prevents the form from being sent to the server
                             // (keeps it client/browser-side and prevents
                             // the browser from awkward reloading)

      var username = inputUsername.value; // the value will be a String
      var genderM = inputGenderM.checked; // the value will be a Boolean
      var genderF = inputGenderF.checked; // the value will be a Boolean
      var tandc = inputTandC.checked; // the value will be a Boolean

      console.log([username, genderM, genderF, tandc]);

      // validation
      if (username === "" || (!genderM && !genderF) || !tandc) {
        console.log("not valid");
        errorMsg.classList.remove('hidden');
        successMsg.classList.add('hidden');
      } else {
        console.log("valid");
        errorMsg.classList.add('hidden');
        successMsg.classList.remove('hidden');
      }
    })
```


## Make it a little bit prettier for the user

Let's add a tiny bit of CSS to make it nicer for the user.  

Add these CSS rules to your `<style>` tag:

```
    .msg-error, .msg-success { padding: 10px; margin: 10px 0; color: #fff; }
    .msg-error { background-color: red; }
    .msg-success { background-color: blue; }
```

## Let's wrap the validation inside a function for cleaner code

The function will be taking several arguments (values from the input fields), validate these values, and carry on with blocks of code depending on whether the form validates or not. Here's how it will look like:

```
      ...

      console.log([username, genderM, genderF, tandc]);

      validateInputFields(username, genderM, genderF, tandc);
    })

    function validateInputFields(username, genderM, genderF, tandc) {
      // validation
      if (username === "" || (!genderM && !genderF) || !tandc) {
        console.log("not valid");
        errorMsg.classList.remove('hidden');
        successMsg.classList.add('hidden');
      } else {
        console.log("valid");
        errorMsg.classList.add('hidden');
        successMsg.classList.remove('hidden');
      }
    }
```

The function `validateInputFields` takes four *arguments* (or *parameters*; sometimes shortened to *args* or *params*), namely: `username`, `genderM`, `genderF`, and `tandc`. These are all the variables that gather user input from `<input>` tags. We simply *pass* them to the function. 

Notice that the `function` is defined outside of the `EventListener`, just before the `</script`> closing tag.

## Full code

This is what the full code should look like:

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Document</title>
  <style>
    .hidden { display: none; }
    .msg-error, .msg-success { padding: 10px; margin: 10px 0; color: #fff; }
    .msg-error { background-color: red; }
    .msg-success { background-color: blue; }
  </style>
</head>
<body>

  <div id="Wrapper">

    <div id="ErrorMsg" class="hidden msg-error">Error. Make sure to fill in all the fields in the form.</div>
    <div id="SuccessMsg" class="hidden msg-success">Success! Thanks for submitting your form.</div>

    <form>

      <input id="InputUsername" type="text" placeholder="username"><br>
      <input id="InputGenderM" type="radio" name="gender"> Male
      <input id="InputGenderF" type="radio" name="gender"> Female <br>
      <input id="InputTandC" type="checkbox"> I agree to the Terms and Conditions <br>
      <input id="SubmitButton" type="submit" value="submit">

    </form>

  </div>

  <script>

    var submitButton = document.querySelector('#SubmitButton'); // targets the submit button
    var inputUsername = document.querySelector('#InputUsername'); // targets the username input
    var inputGenderM = document.querySelector('#InputGenderM'); // targets the male gender input
    var inputGenderF = document.querySelector('#InputGenderF'); // targets the female gender input
    var inputTandC = document.querySelector('#InputTandC'); // targets the TandC input
    var errorMsg = document.querySelector('#ErrorMsg'); // targets the error message
    var successMsg = document.querySelector('#SuccessMsg'); // targets the success message

    submitButton.addEventListener('click', function(event) {
      event.preventDefault(); // prevents the form from being sent to the server
                             // (keeps it client/browser-side and prevents
                             // the browser from awkward reloading)

      var username = inputUsername.value; // the value will be a String
      var genderM = inputGenderM.checked; // the value will be a Boolean
      var genderF = inputGenderF.checked; // the value will be a Boolean
      var tandc = inputTandC.checked; // the value will be a Boolean

      console.log([username, genderM, genderF, tandc]);

      // validation
      if (username === "" || (!genderM && !genderF) || !tandc) {
        console.log("not valid");
        errorMsg.classList.remove('hidden');
        successMsg.classList.add('hidden');
      } else {
        console.log("valid");
        errorMsg.classList.add('hidden');
        successMsg.classList.remove('hidden');
      }
    })

  </script>
</body>
</html>

```
