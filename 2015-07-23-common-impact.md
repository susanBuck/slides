# Beginner HTML & CSS for Nonprofits
## Thursday, July 23, 2015 2:30-4:30pm

URL For these notes: <http://thewc.co/s/common-impact>

Live broadcast: <http://thewc.co/live>

Susan Buck / [Women's Coding Collective](http://thewc.co) / [@WeAreWCC](https://twitter.com/WeAreWCC)

Patricia Vaccaro-Coburn / [Common Impact](http://commonimpact.org/) / [@CommonImpact](https://twitter.com/commonimpact)

Survey: <http://goo.gl/LSrcFA>

# HTML: The code behind web pages
* All web pages are made up of HTML
* *View Source* on <http://phpwomen.org>
* The role of CSS


# Code Editors
* Application: Atom <https://atom.io>
* Browser based: CodePen <http://codepen.io>


# Tag basics
Tags are used to surround content, for example, a heading tag:

```html
<h1>Welcome to Susan's Web Site</h1>
```

The forward slash in the second tag indicates it's the **end tag**.

More tags: [MDN Element reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element?redirectlocale=en-US&redirectslug=HTML%2FElement)

**Practice:** Add a heading and a subheading in the HTML panel of CodePen.


# Tag teamwork
Some tags work together with other tags.

An `<ul>` ([unordered list](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul)) tag teams up with `<li>` ([list item](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li)) tags

	Here are some of my favorite web sites:

```html
<ul>
  <li>Google</li>
  <li>Women's Coding Collective</li>
  <li>Mozilla Developer Network</li>
</ul>
```

**Practice:** Add a list of your three favorite websites below your headings.


# Links
Some start tags have **attributes** to describe information about that element.

Example, the `<a>` element ([anchors](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a) i.e., links) has the `href` attribute which dictates where a link should go.

```html
<a href='http://wikipedia.org'>Wikipedia: The Free Encyclopedia</a>
```

`target` might specify a link should open in a new tab

```html
<a href='http://wikipedia.org' target='_blank'>Wikipedia: The Free Encyclopedia</a>
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
	background-color:orange;
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

**Practice:**

* Change the background-color of the `h1` elements to yellow.
* Add `5px` of padding to the image.
* Add one other style property from the reference list to any of the elements on your page.


# Going live

+ [SiteGround](http://siteground.com/index.htm?afcode=bf90ce97069361478ba4f2426b5f9d4d)
+ [WordPress](http://wordpress.org)
+ [Site Builders](http://www.websitebuilderexpert.com)
