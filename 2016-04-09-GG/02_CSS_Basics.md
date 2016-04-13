## Workspace
<<<<<<< HEAD
For this workshop we'll be working in <http://codepen.io>
=======
In this workshop I'll be working in the code editor [Atom](http://atom.io)
>>>>>>> a72bc3917a740ab977bbcba7ebc43df3165439d6


## HTML Review
HTML is a markup language consisting of about 100 tags describing the structure of your page.

[HTML Element reference](https://developer.mozilla.org/en/HTML/Element)

```html
<!DOCTYPE html>

<html>
<head>
	<title>Practice</title>
</head>
<body>

</body>

</html>
```

But this is only half the picture; HTML alone is insufficient since all it does is describe the content of a page - this is a footer, this is a paragraph, this is a list, this is the body, etc.

The missing piece of the puzzle is CSS to add style.


## What is CSS?
* Cascading Style Sheets
* CSS is a way to describe how the content on your page should look



## Applying styles

There are three ways you can incorporate CSS into your HTML code:

1. Inline
2. Internal
3. External (Most similar to what we're doing in CodePen)

<img src='http://thewc.co/images/tasks/css_three_methods_summary.png'>


## Basic CSS Syntax
* CSS is made up of `property:value` pairs assigned to HTML tags.
* These `property:value` pairs are called **declarations**.




## Demonstration

This is the HTML code we'll be applying styles to:

```html
<h1>Statement</h1>

<h2>March 2014</h2>
<div class='income'>$200</div>
<div class='expenses'>$100</div>

<h2>February 2014</h2>
<div class='income'>$450</div>
<div class='expenses'>$240</div>

<h2>January 2014</h2>
<div class='income'>$150</div>
<div class='expenses'>$530</div>
```

Tasks:

* Make the `<h1>`s have a light grey background with a little bit of padding
* Make the income lines green
* Make the expenses line red
* Make both the income and expenses line a mono-spaced font
* Remove the space between the h2's and the numbers below them

[CSS reference list](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)



## Web Inspectors
* How to open
* Selecting via the elements window vs. with the magnify glass
* Crossed out styles are ones that have been overwritten
* Computed styles
* None of the changes are permanent



## Practice
Recreate the following design:

<img src='http://making-the-internet.s3.amazonaws.com/css-basics-exercise.png' style='border:1px solid black'>

<<<<<<< HEAD
Use an external style sheet.
=======
Starting point: <http://codepen.io/wcc/pen/vGpqEE?editors=1100>
>>>>>>> a72bc3917a740ab977bbcba7ebc43df3165439d6

Approach the design from the outside in&mdash; specifically by beginning with the outer box and then moving in from there. You don't want to get hung up on little details like the style of your bullet points before you get the bigger pieces together.

You don't have match the exact width, height, font sizes or shades of color; just try to get as close as you can.

Think about using the best tag and selector for the job. For example, if you have a large heading, an h1 tag would be more spot-on than a generic div tag.

This exercise is designed to get you digging through the [CSS reference list](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference); you'll want to look into some properties we haven't covered yet such as margin, padding and styling links.
