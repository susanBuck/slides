## Client vs. Server Code

[Web Dev Puzzle](http://thewc.co/images/tasks/javascript-web-dev-puzzle.png)

Web Site:

* A main landing page with the UFL Logo and description of the league
* A schedule of games for the current season (Fall or Spring) for the three participating teams
* A link to a PDF registration form that players can download and fax in
* Basic contact information for the league organizers

Versus Web Application:

* A main landing page with the UFL Logo and description of the league
* A player interface where users can a) register, b) pay dues, c) see what upcoming games they have, etc.
* An admin interface where the UFL owners can administer a) teams, b) league standings, c) who has paid their dues, etc.

## Meet PHP

<img src='http://thewc.co.s3.amazonaws.com/challenges/php-graph.png'>

Pros:

* Low barrier to entry
* Market leader: according to W3Techs, of sites using server-side languages, about 80% are using PHP.
* Availability: Available on almost all common web hosting platforms.
* Resources: Communities, sites, tutorials, etc. 
* Ubiquity: WordPress, Joomla and Drupal. E-commerce: Zencart, osCommerce and Magento.

Cons:

* Wild wild west

## Time-of-day Demonstration

This is what we want to create: <http://php.wcc-hosting.com/clock/>

The page should change depending on the time of day:

<img src="http://making-the-internet.s3.amazonaws.com/php-morning-afternoon-evening-night.png">

If your user visits your page between 5am and 10:59am in the morning, they should see this image:

	http://thewc.co.s3.amazonaws.com/challenges/php-morning.png


If they visit between 11am and 3:59pm in the afternoon, they should see this image:

	http://thewc.co.s3.amazonaws.com/challenges/php-afternoon.png


If they visit between 4pm and 7:59pm in the evening, they should see this image:

	http://thewc.co.s3.amazonaws.com/challenges/php-evening.png


If they visit between 8pm and 4:59am at night, they should see this image:

	http://thewc.co.s3.amazonaws.com/challenges/php-night.png


The background color of the page should match the scenery image they're seeing. 
For example, if it's morning time, the background color should be purple (#856f86).

<img src='http://making-the-internet.s3.amazonaws.com/php-colors.png'>


## Procedure

We'll be building our demo on a testing server at <http://thewc.co/hosting>.

Create a page called logic.php and connect it to index.php using the [require()](http://us1.php.net/require) method:

	<?php require 'logic.php'; ?>


First things first, we need to set the time in logic.php using PHP's [date()](http://us3.php.net/manual/en/function.date.php) method:


	# Get the time... This will be used to display the time on the page
	# g = 12-hour format of an hour without leading zeros
	# : = Just a colon
	# i = Minutes with leading zeros
	# a = Lowercase am or pm
	$time = date('g:ia');


And display it in index.php:

	<h1>It is <?php echo $time?></h1>
	
	
If the time is off, we have to set the correct timezone:

	# Set the timezone
	# Substitute in your own timezone; Ref: http://us3.php.net/manual/en/timezones.php
	date_default_timezone_set('America/New_York');
	
Now let's hone in on the hour for the purposes of figuring out what period of the day it is:

	# Figure out what the hour is using the 'G' format: 24-hour format of an hour w/o leading zeros
	$hour = date('G');
	
	
Once you know the hour, you can use and if/else statement to determing if it's morning/afternoon/evening/night. 
The statement that gets executed will set the $image variable.

	# Between 5am (5:00 hours) and 10:59am (10:59 hours)
	if($hour >= 5 AND $hour < 11) {
		$image = 'php-morning.png';
	}
	# Between 11am (11:00 hours) and 3:59pm (15:59 hours)
	elseif($hour >= 11 AND $hour < 16) {
		$image = 'php-afternoon.png';
	}
	# Between 4pm (16:00 hours) and 7:59pm (19:59 hours)
	elseif($hour >= 16 AND $hour < 20) {
		$image = 'php-evening.png';
	}
	# Anything after 8pm (20:00 hours)
	else {
		$image = 'php-night.png';
	}
	
Which you can then use in index.php:

	<img src='http://thewc.co.s3.amazonaws.com/challenges/<?=$image?>' alt='Time of day scene'>
	
Test your logic by hardcoding the hour:

	# Tests we can uncomment when testing the code
	# $hour = 6;  # Test morning
	# $hour = 12; # Test afternoon
	# $hour = 6;  # Test evening
	# $hour = 23; # Test night

Once that's working, time for the background-color, which you'll set up some classes for:

	.morning {
		background-color:#865f86; /* purple */
	}
	
	.afternoon {
		background-color:#2c87c8; /* royal blue */
	}
	
	.evening {
		background-color:#c7b02f; /* yellowish mustard */
	}
	
	.night {
		background-color:#180629; /* dark purple */
	}

The idea is to set the appropriate class on the body, for example:

	<body class='morning'>

But instead of hard coding the class, you'll want to create a variable, which you can echo out just like you did $image:	
	
	<body class='<?php echo $class; ?>'>

To set the class, you can piggy-back on your existing if statement:

	# Between 5am (5:00 hours) and 10:59pm (10:59 hours)
	if($hour >= 5 AND $hour < 11) {
		$image = 'php-morning.png';
		$class = 'morning';
	}
	# Between 11am (11:00 hours) and 3:59pm (15:59 hours)
	elseif($hour >= 11 AND $hour < 16) {
		$image = 'php-afternoon.png';
		$class = 'afternoon';
	}
	# Between 4pm (16:00 hours) and 7:59pm (19:59 hours)
	elseif($hour >= 16 AND $hour < 20) {
		$image = 'php-evening.png';
		$class = 'evening';
	}
	# Anything after 8pm (20:00 hours)
	else {
		$image = 'php-night.png';
		$class = 'night';
	}