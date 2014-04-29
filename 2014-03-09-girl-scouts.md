## 0. Info

**http://thewc.co/s/girlscouts2**


## 1. Setup

* Starting Code: <http://codepen.io/wcc/pen/joLuw>
* Final demo, "if/else" version: <http://codepen.io/wcc/pen/kBywA>
* Final demo, "matrix" version: <http://codepen.io/wcc/pen/JnKwC>

Visit <http://codepen.io/wcc/pen/joLuw> and click "Fork" from the top menu.

This will give you a version of the starting point code to work from.



## 2. Files

* Rock file: `http://misc001.s3.amazonaws.com/rock.png`
* Paper file: `http://misc001.s3.amazonaws.com/paper.png`
* Scissors file: `http://misc001.s3.amazonaws.com/scissors.png`





## 3. HTML Images

This is what the code looks like to create an image in HTML:

	<img src='http://misc001.s3.amazonaws.com/rock.png' id='rock' class='piece'>

`src`, `id` and `class` are all attributes of this image.

Id is a unique identifier...kind of like your first name.

Class is an identifier that multiple elements can share...kind of like your last name.




## 4. Variables

Variables are used in programming to remember bits of information.

For example:

	var my_name = 'Susan';
	
	var results = 'Tie!';
	
	var age = 29;

In JavaScript, variables always start with the keyword `var`.
	
	
	
	
	
## 5. Arrays

Arrays are a more complex type of variable because they allow you to store multiple bits of information in them.

Here's how we'd create an empty array called scenarios:

	var scenarios = [];

We could then fill that array. For example, let's start with the rock(0) scenarios:

	scenarios[0] = [];
	
And then fill the rock scenarios with rock(0), paper(1), scissors (3):

	scenarios[0][0] = 'Tie :-|';
	scenarios[0][1] = 'Computer :-(';
	scenarios[0][2] = 'You :-)';





## 6. Random number

Here's the line of JavaScript that will generate either a 0, 1 or 2 (three numbers total):

	Math.floor(Math.random()*3);




## 7. Change the image path

	$('#computer').attr('src','http://misc001.s3.amazonaws.com/rock.png');
	



	
## 8. Get an attribute

	var players_move = $(this).attr('id');





## 9. Decisions making

In programming, you can use *If statements* to get your code to make decisions...

	if(grade >= 90) {
		var letter_grade = 'A';
	}
	elseif(grade >= 80 AND < 90) {
		var letter_grade = 'B';
	}
	elseif(grade >= 70 AND < 80) {
		var letter_grade = 'C';
	}
	elseif(grade >= 60 AND < 70) {
		var letter_grade = 'D';
	}
	elseif(grade < 60) {
		var letter_grade = 'E';
	}






## 10. Change contents

	$('#results').html('You are the winner!');
	

