# HTML/CSS Crash Course
## Bok Center - Learning Labs workshop

Thursday Mar 3, 2016 2-4pm

Notes: <http://thewc.co/s/bok2016>

Susan Buck / [Women's Coding Collective](http://thewc.co) / @WeAreWCC

Early birds: If you arrive early, download, install and open <https://atom.io>




## HTML: The code behind web pages
* All web pages are structured using HTML code
* Example with *View Source*
* Beyond web sites...
* [MDN Element reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element?redirectlocale=en-US&redirectslug=HTML%2FElement)
* The role of CSS





## Code Editors
* What is a code editor?
* Download, install: <https://atom.io>




## Our first page
* Save the following code as `example.html` on your Desktop.
* Load this file in your web browser


```html
<!DOCTYPE html>
<html>
<head>

	<title></title>
	<meta charset='utf-8'>

	<link rel='stylesheet' href='' type='text/css'>

</head>
<body>



</body>
</html>
```




## Tag basics
Tags are used to surround content, for example, here's a heading tag:

```html
<h1>Welcome to Susan's Web Site</h1>
```

The forward slash in the second tag indicates it's the **end tag**.

**Practice:** Create a heading and a subheading in the `<body></body>` of your page.




## Tag teamwork
Some tags work together with other tags.

An `<ul>` ([unordered list](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul)) tag teams up with `<li>` ([list item](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li)) tags

```html
Here are some of my favorite web sites:

<ul>
  <li>Google</li>
  <li>Wikipedia</li>
  <li>Tumblr</li>
</ul>
```

**Practice:** Add a list of three different websites below your headings.




## Links
Some start tags have **attributes** to describe information about that element.

Example, the `<a>` element ([anchors](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a) i.e., links) has the `href` attribute which dictates where a link should go.

```html
<a href='http://wikipedia.org'>The Free Encyclopedia</a>
```

`target` might specify a link should open in a new tab

```html
<a href='http://google.com' target='_blank'>The Free Encyclopedia</a>
```

**Practice:** Edit your unordered list so that each of your favorite web sites includes a link to that website.




## Images
Images have a `src` attribute to specify the image's location.

```html
<img src='kitten.png'>
```

The `alt` attribute is required for non-decorative images:

```html
<img src='kitten.png' alt='An adorable kitten'>
```

**Practice 1:** Find an image on Wikipedia of your favorite animal.

Right click on that image and find the option to copy the image URL.

* Chrome: *Copy Image URL*
* Firefox: *Copy Image Location*
* Safari: *Copy Image Address*

On your page, use this URL to display the image in an `<img>` element.

Example:

```html
<img alt='Adorable kitten' src='http://upload.wikimedia.org/wikipedia/commons/thumb/0/06/Kitten_in_Rizal_Park%2C_Manila.jpg/340px-Kitten_in_Rizal_Park%2C_Manila.jpg'>
```

**Practice 2:** For fun, using the letters from <http://lettergame.s3.amazonaws.com/details.html>, spell out your name on your page.




# Adding style

CSS stands for *Cascading Style Sheets*.

CSS is a way to describe how the content on your page should look.

In the `<head></head>` of your page, add the following code:

```css
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
```

CSS is made up of `property:value` pairs assigned to HTML elements.

These `property:value` pairs are called **declarations**.

[CSS reference list](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)

**Practice:** Make some edits to the above CSS and see how it changes your page. Apply one other style found in the CSS reference list.



## Publishing sites online

Example web hosting provider: [SiteGround](http://www.siteground.com/index.htm?afcode=bf90ce97069361478ba4f2426b5f9d4d)

Example domain provider:[Namecheap](http://namecheap.com)
