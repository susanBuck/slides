## Workspace
For this workshop we'll be working in <http://codepen.io>


## CSS Basics Recap
CSS styles are made up of `property:value;` pairs called **declarations**. Ex: `color:red;`


## Why layouts are tricky

<img src='http://thewc.co/images/tasks/css2_website_sketch.jpg'>

Basic styling: colors, fonts, borders...easy

Layouts: more complex

These are the properties used layouts:

* position (static, absolute, relative or fixed)
* top, left, bottom, right
* margin
* padding
* float (left, right)
* clear (left, right or both)

[CSS Cheat Sheet](http://thewc.co.s3.amazonaws.com/challenges/css-layouts-cheat-sheet.pdf)


## position:static

* Neutral, no-position position property; it abides by what we call the normal flow of the page.
* Normal flow of the page = word processor style layout
* Default position if you don't specify a position
* Don't see static used often, but useful if you ever need to &ldquo;reset&rdquo; a position back to the default


## position:fixed
* Specify exactly where in the browser window you want an element to land
* Set with offset properties (top, left, bottom, right)
* Positions in relation to the browser window
* Takes the element out of the normal flow of the page
* Ignore scrolling
* Good for sticky menus
* In the wild: [Fat Man Collective](http://web.archive.org/web/20130122060307/http://fat-man-collective.com/hello.php) or [Girl with a Camera](http://girlwithacamera.co.uk/)

### Example 1

```html
<style>   
	.simpleBox {
	    width:100px;
		height:100px;
		background-color:lightblue;
		position:fixed;
		top:0px; 
		left:100px;
	}
</style>

<div class='simpleBox'></div>
```
	
### Example 2
<http://codepen.io/wcc/pen/Deahi>


## position:absolute

* Positions elements relative to their parent element
* If there is no parent element, then it positions according to the browser
* Uses the offset properties (top, left, bottom, right)
* Only works if the parent element has a position property set (fixed, absolute, relative will work...static will not)
* An absolutely positioned element is taken out of the normal flow of the page

```html
<style>
    #wrapper {
		 border:1px solid black;
		 width:600px;
		 height:200px;
		 position:fixed;
		 top:50px;
		 left:50px;
	 }
	 
	 #simpleBox {
		 background-color:lightblue;
		 width:50px;
		 height:50px;
		 position:absolute;
		 top:25px;
		 left:50px;
	 }
</style>
    
<div id='wrapper'>
	<div id='simpleBox'></div>
</div>
```




## position:relative

The relative position property shift elements; It looks at where the element would be without any position properties, and then "shifts" 
it from that spot.

```html
<style>
	#thirdImage {
		position:relative;
		top:-10px;
		left:-10px;
	}
</style>

<img src='http://practice-pixels.s3.amazonaws.com/kitten_250x250.jpg'>
<img src='http://practice-pixels.s3.amazonaws.com/kitten_250x250.jpg'>
<img src='http://practice-pixels.s3.amazonaws.com/kitten_250x250.jpg' id='thirdImage'>
```


### Absolute's sidekick

```html
<style>
	 #wrapper {
		border:1px solid black;
		width:600px;
		height:200px;

		/* Setting just position relative with no 
		top left bottom right values will let the element
		sit just where it normally would, yet it will 
		allow it to place nice with its absolute child */
		position:relative;
	 }
	 
	 #simpleBox {
		background-color:lightblue;
		width:50px;
		height:50px;
		position:absolute;
		top:25px;
		left:50px;
	 }
</style>

<div id='wrapper'>
  <div id='simpleBox'></div>
</div>
```


## Layout types
### Fixed
With fixed layouts, you're mostly dealing with set widths. This means that no matter how big or small your user's screen or browser is, the design is going to stay the same.

[The Design Cubical Blog](http://www.thedesigncubicle.com/)

<small>
Note: Fixed layouts != position:fixed. Fixed layouts and fixed position are actually quite different beasts. Don't let the regrettably confusing terminology get you muddled.
</small>

### Fluid
Fluid (aka liquid) layouts are flexible; they expand and contract with the browser window. Here are some common characteristics you'll see with fluid designs:

Type will wrap differently depending on the browser width.

Blank space (aka "white space") between items can expand and contract.

The site seems to "fill" the browser no matter how big it is.

Examples:

* <http://webtypography.net/intro/>
* <http://devdocs.io/>

### Responsive
[The Boston Globe](http://www.bostonglobe.com/)
[Happy Cog](http://happycog.com/)

Not only does the site resize, it rearranges for optimal use of the space
Replacement for having multiple versions of your site

Which one should you choose?
Things to consider

* Site's content
* Intended audience
* Resources / time / expertise
