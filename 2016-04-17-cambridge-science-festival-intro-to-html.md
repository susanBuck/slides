# Intro to HTML for Girls & Their Moms--or Grandmas, Aunts, Big Sisters, etc.

Cambridge Science Festival - April 17, 2015 2:00-4:00pm

Notes: <http://thewc.co/s/csf2016>

Susan Buck / [Women's Coding Collective](http://thewc.co) / @WeAreWCC


# HTML: The code behind web pages
* All web pages are made up of HTML
* Tour via View Source
* The role of CSS
* [MDN Element reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element?redirectlocale=en-US&redirectslug=HTML%2FElement)


# Code Editors
* What is a code editor?
* Application: Atom <http://atom.io>
* Browser based: CodePen <http://codepen.io>
* Some benefits of a code editor
	* Line numbers
	* Syntax highlighting
	* Code hinting


# Tag basics
Tags are used to surround content, for example, here's a heading tag:

```html
<h1>Welcome to Susan's Web Site</h1>
```

The forward slash in the second tag indicates it's the **end tag**.

**Practice:** Add a heading and a subheading in the HTML panel of CodePen.





# Tag teamwork
Some tags work together with other tags.

An `<ul>` ([unordered list](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul)) tag teams up with `<li>` ([list item](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li)) tags

```html
Here are some of my favorite web sites:

<ul>
  <li>Google</li>
  <li>Women's Coding Collective</li>
  <li>Tumblr</li>
</ul>
```

**Practice:** Add a list of your three favorite websites below your headings.




# Links
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



# Images

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

**Practice 2:** Using the letters from <http://lettergame.s3.amazonaws.com/details.html>, spell out your name on your page.


# Adding style

CSS stands for Cascading Style Sheets.

CSS is a way to describe how the content on your page should look.

In the CSS Panel of CodePen, add the following CSS code:

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



# Going live

Right now you're the only one that can view your web page&mdash; let's change that!

Web hosting gives you a place to store your work online, where the rest of the world can access it.

Example: [SiteGround](http://www.siteground.com/index.htm?afcode=bf90ce97069361478ba4f2426b5f9d4d)

For this class, we'll use the free web site playground, [NeoCities](https://neocities.org).

## Step 1)
Create an account at Neocities: <https://neocities.org>.


## Step 2) Add your CSS styles
In Neocities, find the button to add a __New File__ and create a new file called `style.css`.

Find the __Edit__ button for this file you just created.

In the code editor window that opens, copy and paste the CSS code you wrote in CodePen today. (Copy just the CSS code, *not* the HTML code)

Click __Save__ to save your changes to `style.css`, and then go back to your __Dashboard__.


## Step 4)
Find the existing file `index.html` and click __Edit__.

Delete *all* the default code that is currently in that file.

Copy and paste in this HTML template:

```html
<!DOCTYPE html>
<html>
<head>

	<title>My First Web Page</title>
	<meta charset='utf-8'>

	<link rel='stylesheet' href='style.css' type='text/css'>

</head>
<body>



</body>
</html>
```

## Step 5)
Within the `<body></body>` of the code you just pasted above, copy and paste the HTML code you wrote today in CodePen. (Copy just the HTML code, *not* the CSS code).

Once your code is pasted click __Save__.


## Step 6)
View your finished product at `http://your-username.neocities.org`
