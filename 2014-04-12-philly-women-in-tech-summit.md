# CSS: Essentials of Website Styling

April 12, 2014
10:15-11:45am (1hr 30min)

Don't already have a favorite code editor? 
Install <http://sublimetext.com>



# What is CSS?

* Sibling to HTML
* Cascading Style Sheets
* HTML is a mark-up language consisting of about [100 different tags](https://developer.mozilla.org/en/HTML/Element):

	<!DOCTYPE html>
	<html>
	<head>
	
		<title></title>
		<meta charset='utf-8'>
		
	</head>
	<body>
	
		<h1>Hello World!</h1>
		
		<p>Welcome to my very simple web page.</p>
	
		<p>Here are three of my favorite things:</p>
		<ul>
			<li>Kittens</li>
			<li>Kittens</li>
			<li>Kittens</li>
		</ul>
		
	</body>
	</html>
	

# Integrating into HTML

1. Inline
2. Internal
3. External


# Syntax basics


CSS is made up of `property:value;` pairs assigned to HTML elements

These `property:value;` pairs are called **declarations**

For example: `color:red;` or `margin:5px;`

Reference for all the available CSS properties: <https://developer.mozilla.org/en-US/docs/Web/CSS/Reference>


# Practice

	<h1>Monies</h1>
	
	<h2>March 2014</h2>
	<div class='income'>$200</div>
	<div class='expenses'>$100</div>
	
	<h2>February 2014</h2>
	<div class='income'>$450</div>
	<div class='expenses'>$240</div>
	
	<h2>January 2014</h2>
	<div class='income'>$150</div>
	<div class='expenses'>$530</div>
	
## Tasks:

* Make the h1 have a light grey background with a little bit of padding
* Make the income lines green
* Make the expenses line red
* Make both the income and expenses line a mono-spaced font
* Remove the space between the h2's and the numbers below them


# Web Inspectors

* How to open in different browsers
* Selecting via the elements window vs. with the magnify glass
* Crossed out styles are ones that have been overwritten
* Computed styles
* None of the changes are permanent

# Layouts

CSS Properties used to control layouts and positioning:

* position (static, absolute, relative or fixed)
* top, left, bottom, right
* margin
* padding
* float (left, right)
* clear (left, right or both)

* [Cheat Sheet](http://thewc.co.s3.amazonaws.com/challenges/css-layouts-cheat-sheet.pdf)


# More Practice

Recreate the following page:

<img src='http://making-the-internet.s3.amazonaws.com/css-basics-exercise.png?2x' width='500' style='border:1px solid black'>

### Specifications:

* Use an external style sheet.
* Background pattern image: <http://misc001.s3.amazonaws.com/cross-cross-pattern.png>
* You don't have match the exact width, height, font sizes or shades of color; just try to get as close as you can.
* Think about using the element for the job. For example, if you have a large heading, an h1 tag would be more spot-on than a generic div tag.
* This exercise is designed to get you digging through the [CSS reference list](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference); you'll want to look into some properties we haven't covered yet such as margin, padding and styling links.

<small>Solution: <http://codepen.io/wcc/pen/uwLsq></small>
