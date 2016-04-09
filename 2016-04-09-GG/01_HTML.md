## HTML: The code behind web pages
* All web pages are made up of HTML
* Tour via *View Source*
* The role of CSS
* [MDN Element reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element?redirectlocale=en-US&redirectslug=HTML%2FElement)


## Code Editors
* What is a code editor?
* <https://atom.io>
* For this workshop we'll use <http://codepen.io>


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
<h2>Interesting Sites</h2>

<ul>
  <li>Geek Girl Tech Conferences</li>
  <li>Women's Coding Collective</li>
  <li>Wikipedia</li>
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


# Going live

Recommendations:
+ Hosting: [SiteGround](http://www.siteground.com/index.htm?afcode=bf90ce97069361478ba4f2426b5f9d4d)
+ Domains: [Namecheap](https://www.namecheap.com/?aff=61057)
