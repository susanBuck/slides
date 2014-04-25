# Intro to HTML for Girls & Their Moms--or Grandmas, Aunts, Big Sisters, etc.

Cambridge Science Festival - April 27, 2014

2:00-4:00pm

Susan Buck / [Women's Coding Collective](http://thewc.co) @WeAreWCC

Notes: http://thewc.co/s/

## Code Editors
* What is a code editor?
* <http://sublimetext.com>
* Some benefits of a code editor
	* Line numbers
	* Syntax highlighting

## What is HTML?
* All web pages are made up of HTML
* Tour via View Source
* The role of CSS
* [MDN Element reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element?redirectlocale=en-US&redirectslug=HTML%2FElement)


## Your first web page

1. Copy the following code into a blank document in Sublime
2. Save the file as practice.html to somewhere accessible like your Documents or Desktop
3. Once the file is saved, right click in Sublime and choose *Open in browser*

	<!DOCTYPE html>
	<html>
	<head>
	
		<meta charset='utf-8'>
		
		<title>My Web Site</title>		

	</head>
	
	<body>
	
		<h1>Hello World!</h1>
	 
	</body>
	
	</html>

### doctype
Doctype gives the browser information about the kind of HTML you're writing so it knows how to render it. There are many kind of doctypes, but here we're using the latest HTML5 doctype.

### Head
The head element of the page is where you specify behind the scenes information about your page, not anything that actually gets rendered on the page. 

In this template, we start off the head with the `<meta charset='utf-8'>` element followed by the `<title>` element.


### Body
The body is where content content of your page goes.

### Comments
The `<!-- -->` syntax is used for HTML comments.
Use them to organize your code, leave reminders for yourself, etc.





## Non-void Elements
Some elements surround content. When they do, they have a start tag and an end tag.
Here the [emphasis element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/em) surrounds text to indicate emphasis.

	<h1>Welcome to Susan's Web Site</h1>

The forward slash in the second tag indicates it's the **end tag**.
	
## Tag teamwork
Some tags work together with other tags
An `<ul>` ([unordered list](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul)) tag teams up with `<li>` ([list item](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li)) tags

	Here are some of my favorite web sites:

	<ul>
	  <li>Google</li>
	  <li>Women's Coding Collective</li>
	  <li>Tumblr</li>
	</ul>



## Attributes
Some start tags have **attributes** to describe information about that element.

Example, the `<a>` element ([anchors](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a) i.e., links) has the `href` attribute which dictates where a link should go.


~~~~
<a href='http://wikipedia.org'>The Free Encyclopedia</a>
~~~~

`target` might specify a link should open in a new tab

~~~~
<a href='http://google.com' target='_blank'>The Free Encyclopedia</a>
~~~~

**Practice:** Edit your unordered list so that each of your favorite web sites includes a link to that website.


Images have a `src` attribute to specify the image's location

~~~~
<img src='http://placekitten.com/200/200'>
~~~~

The `alt` attribute is required for non-decorative images:

~~~~
<img src='http://placekitten.com/200/200' alt='Adorable kitten'>
~~~~

### Practice

Find an image on Wikipedia of your favorite animal.

Right click on that image and find the option to *Copy Image Url...*; this will copy the path to the image.

Create an image on your page and paste in the URL.

Example:

	<img src='http://upload.wikimedia.org/wikipedia/commons/thumb/0/06/Kitten_in_Rizal_Park%2C_Manila.jpg/340px-Kitten_in_Rizal_Park%2C_Manila.jpg'>

Now, using the letters from <http://lettergame.s3.amazonaws.com/details.html>, spell out your name on your page.


## Adding style

CSS stands for Cascading Style Sheets.

CSS is a way to describe how the content on your page should look.

In the `<head>` of your page, add the following CSS code:

	<style>
		
		body {
			background-color:Orange;
			color:white;
		}
		
		h1 {
			font-family:Georgia;
		}
		
		img {
			border:1px solid black;
			padding:5px;
		}
	
	</style>

CSS is made up of `property:value` pairs assigned to HTML elements.

These `property:value` pairs are called **declarations**.

[CSS reference list](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)
	
	

## Going live

Right now you're the only one that can view your web page&mdash; let's change that!

Web hosting gives you a place to store your work online, where the rest of the world can access it.

Example: [SiteGround](http://www.siteground.com/index.htm?afcode=bf90ce97069361478ba4f2426b5f9d4d)

For this class, we'll use the free web site playground, NeoCities.

1. Create an account at Neocities: <https://neocities.org>.
2. In Neocities, find the option to edit your index.html file.
3. In this file, paste in the code you've created in this class.
4. View your finished product at `http://your-username.neocities.org`




