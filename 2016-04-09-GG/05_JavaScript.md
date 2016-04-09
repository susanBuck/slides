## Workspace
For this workshop we'll be working in <http://codepen.io>



## What is JavaScript?
[Web Development Puzzle](http://making-the-internet.s3.amazonaws.com/misc-puzzle.png)

Like CSS, JavaScript is more code that gets incorporated into your HTML page.

JavaScript allows you to:

* Control the browser
* Communicate asynchronously (Ajax)
* **Alter the page after the page has loaded**

Quick Facts:

* JavaScript != Java
* JavaScript is most commonly used as a client-side script, but it also has server-side implementations.



## Examples
* [Essence: Manipulating CSS](http://codepen.io/wcc/pen/stncu/)
* [Fun/Interactive: Animations](http://photojojo.com/store/awesomeness/sony-smart-lens-qx10-qx100/)
* [Practical: Menus](https://www.google.com/)
* [Practical: Form validation](https://wwws.mint.com/login.event?task=S)
* [Vogue with Konami - U-U-D-D-L-R-L-R-B-A-Enter](http://www.vogue.co.uk/)
* [Ajax: Fetch information live](http://instantdomainsearch.com/)



## Rock, Paper, Scissors

* Starting Code: <http://codepen.io/wcc/pen/joLuw>
* Final demo, "if/else" version: <http://codepen.io/wcc/pen/kBywA>
* Final demo, "matrix" version: <http://codepen.io/wcc/pen/JnKwC>

<!--
1. Explain everything going on in the starting code
2. How would we build this logic if we were playing it without a computer?

3. Create a variable computers move between 0 and 2  Math.floor(Math.random()*3);
4. Convert this numeric move into rock paper or scissors
5. Change the computer's image
-->


### Files
* Rock file: `http://misc001.s3.amazonaws.com/rock.png`
* Paper file: `http://misc001.s3.amazonaws.com/paper.png`
* Scissors file: `http://misc001.s3.amazonaws.com/scissors.png`



### HTML Images
This is what the code looks like to create an image in HTML:

```html
<img src='http://misc001.s3.amazonaws.com/rock.png' id='rock' class='piece'>
```

`src`, `id` and `class` are all attributes of this image.

Id is a unique identifier...kind of like your first name.

Class is an identifier that multiple elements can share...kind of like your last name.



### Variables
Variables are used in programming to remember bits of information.

For example:

```js
var my_name = 'Francis';
var results = 'Tie!';
var age = 30;

In JavaScript, variables always start with the keyword `var`.



---
### Random numbers
Here's the line of JavaScript that will generate either a 0, 1 or 2 (three numbers total):

```js
Math.floor(Math.random()*3);
```



---
### Change the image path

```js
$('#computer').attr('src','http://misc001.s3.amazonaws.com/rock.png');
```


### Get an attribute

```js
var players_move = $(this).attr('id');
```


### Decisions making

In programming, you can use *If statements* to get your code to make decisions...

```js
if(grade >= 90) {
	var letter_grade = 'A';
}
elseif(grade >= 80 AND < 90) {
	var letter_grade = 'B';
}
elseif(grade >= 70 AND < 80) {
	var letter_grade = 'C';
}
elseif(grade >= 60 AND < 70) {
	var letter_grade = 'D';
}
elseif(grade < 60) {
	var letter_grade = 'E';
}
```


### Change contents

```js
$('#results').html('You are the winner!');
```


### Arrays

Arrays are a more complex type of variable because they allow you to store multiple bits of information in them.

Here's how we'd create an empty array called scenarios:

```js
var scenarios = [];
```

We could then fill that array. For example, let's start with the rock(0) scenarios:

```js
scenarios[0] = [];
```

And then fill the rock scenarios with rock(0), paper(1), scissors (3):

```js
scenarios[0][0] = 'Tie :-|';
scenarios[0][1] = 'Computer :-(';
scenarios[0][2] = 'You :-)';
```
