## Code Editors
* What is a code editor?
* <http://sublimetext.com>
* Basic usage and workflow

	* Save your file with a .html extension
	* Right click in the Sublime window and choose "Open in browser..."
	* Refresh the browser whenever you save changes in Sublime

* For this workshop we'll use <http://codepen.io>


## What is HTML?
* All web pages are made up of HTML
* Tour via View Source
* The role of CSS
* Element makeup


## Non-void Elements
Some elements surround content. When they do, they have a start tag and an end tag.
Here the [emphasis element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/em) surrounds text to indicate emphasis.

	Registration forms are due <em>August 9th</em>.

The forward slash in the second tag indicates it's the **end tag**.

## Void Elements
Other elements don't surround content, they live all by themselves.
Here the [break element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br) is used on its own to add new lines:

	First, I'll go to the store<br>
	Then, I'll go to the movies<br>
	Finally, I'll take a nap<br>
	
	
## Tag teamwork
Some tags work together with other tags
An `<ul>` ([unordered list](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul)) tag teams up with `<li>` ([list item](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li)) tags

	Some of my favorite things about Philadelphia (in no particular order)

	<ul>
	  <li>The Phillies</li>
	  <li>Great restaurants</li>
	  <li>Wissahickon Park</li>
	  <li>All those great potholes</li>
	</ul>

Or the `<ol>` (ordered list)

	My favorite things about Philadelphia, in order from most to least

	<ol>
	  <li>The Phillies</li>
	  <li>Great restaurants</li>
	  <li>Wissahickon Park</li>
	  <li>All those great potholes</li>
	</ol>


## Reference

* [MDN Element reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element?redirectlocale=en-US&redirectslug=HTML%2FElement)



## Practice
* Use nesting to combine `<a>` and `<img>` to create an image that is a link. For example, show a picture of a kitten that when clicked, takes you to the wikipedia page about kittens.



## Document structure

We've talked a lot about individual elements with specific tasks, but HTML plays in a bigger role in structuring the page as a whole.

For every HTML page you build, there's a basic template you'll follow:

	<!DOCTYPE html>
	<html>
	<head>
	
		<meta charset='utf-8'>
		
		<title>My Web Site</title>		

	</head>
	
	<body>
	
	  <!-- CONTENT TO BE DISPLAYED GOES HERE IN THE BODY -->
	 
	</body>
	
	</html>
	

Let's break this down...

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
