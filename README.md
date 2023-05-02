Download Link: https://assignmentchef.com/product/solved-comp1012-lab7
<br>
<h2><span class="s1"><b>Error checking</b></span></h2>

<p class="p2"><span class="s1">Read in the file <a href="file:///Users/jubairsheikh/Desktop/Lab%2006/marks.txt"><span class="s6">marks.txt</span></a>. The file format is one number per line. Your program should iterate over all of these numbers, and test to see they they are <b>valid</b> numbers.</span>

<p class="p2"><span class="s1">Create two lists:</span>

<ul class="ul1">

 <li class="li4"><span class="s1">one for valid numbers,</span></li>

 <li class="li4"><span class="s1">one for <i>invalid</i> numbers.</span></li>

</ul>

<p class="p2"><span class="s1">For a number to be valid, the number:</span>

<ul class="ul1">

 <li class="li4"><span class="s1">Must not have any letters inside of it (it must be <i>numeric</i> – use the string function <a href="https://docs.python.org/3/library/stdtypes.html#str.isnumeric"><span class="s6">.isnumeric()</span></a>)</span></li>

 <li class="li4"><span class="s1">Must be greater than or equal to 0</span></li>

 <li class="li4"><span class="s1">Must be less than or equal to 100</span></li>

</ul>

<p class="p2"><span class="s1">For output, your program should print out the average of the valid inputs, and the list of <b>invalid</b> numbers along with their line number and a reason why they are invalid.</span>

<p class="p2"><span class="s1">Sample output for </span><span class="s7">data.txt</span>

<p class="p5"><span class="s1">Average of good data: 45.5</span>

<p class="p5"><span class="s1">Bad data:</span>

<p class="p5"><span class="s1">Value ‘4824’ on line 2 is bad because ‘too big’</span>

<p class="p5"><span class="s1">Value ‘jrfymhnlkt’ on line 3 is bad because ‘not numeric’</span>

<p class="p5"><span class="s1">Value ‘kvryvqoddj’ on line 4 is bad because ‘not numeric’</span>

<p class="p5"><span class="s1">Value ‘-95’ on line 6 is bad because ‘not numeric’</span>

<p class="p5"><span class="s1">…</span>

<p class="p2"><span class="s1"><b>Hint</b>: Use a </span><span class="s7">tuple</span><span class="s1"> to represent cases of invalid data. You can build a </span><span class="s7">tuple</span><span class="s1"> using parenthesis:</span>

<p class="p7"><span class="s8">bad </span><span class="s9">=</span><span class="s8"> (</span><span class="s10">1</span><span class="s8">, </span><span class="s1">“shdj”</span><span class="s8">, </span><span class="s1">“not numeric”</span><span class="s8">)<span class="Apple-converted-space">  </span></span><span class="s11"><i># a tuple!</i></span>

<p class="p2"><span class="s1"><b>Hint 2</b>: You can get line numbers by using the <a href="https://docs.python.org/3/library/functions.html#enumerate"><span class="s6">enumerate</span><span class="s12"> function</span></a></span>

<h2><span class="s1"><b>Optional: Deduction Game</b></span></h2>

<p class="p2"><span class="s1">Write a game where a user has to guess a number from 1 – 99.</span>

<p class="p2"><span class="s1">Your program will generate a random number <b>once</b> (pick a number), and will then prompts the user to repeatedly guess the number until they get it correct.</span>

<p class="p2"><span class="s1">During the game, your program will test the number that the user entered compared to the number it picked. If the number that the user guessed is greater than the random number, tell the user “your guess is too low”. If the number that the user guessed is higher than the random number, tell the user, “your guess is too high”. Let the user continue guessing the number generated until they guess it right.</span>

<p class="p2"><span class="s1">Once the user has successfully guessed the number, tell the user they win, and tell them how many guesses it took them to guess it right.</span>

<p class="p2"><span class="s1">Use a loop to check your user input. Use string’s <a href="https://docs.python.org/3/library/stdtypes.html#str.isnumeric"><span class="s12">.isnumeric()</span></a> to check to see if the user has provided you with a valid number before you use a cast to an integer. Your program <b>should not</b> crash if the user gives you bad input.</span>

<p class="p2"><span class="s1">To create a random number use:</span>

<p class="p5"><span class="s1">import random</span>

<p class="p5"><span class="s1">myRandomNumber </span><span class="s9">=</span><span class="s1"> random.randint(</span><span class="s10">1</span><span class="s1">, </span><span class="s10">99</span><span class="s1">)</span>

<p class="p2"><span class="s1">Sample game:</span>

<p class="p5"><span class="s1">I’ve picked a number between 1 and 99, can you guess it? </span><span class="s13">50</span>

<p class="p5"><span class="s1">Nope, it’s not 50</span>

<p class="p5"><span class="s1">Your guess is too low</span>

<p class="p5"><span class="s1">I’ve picked a number between 1 and 99, can you guess it? </span><span class="s13">99</span>

<p class="p5"><span class="s1">Nope, it’s not 99</span>

<p class="p5"><span class="s1">Your guess is too high</span>

<p class="p5"><span class="s1">I’ve picked a number between 1 and 99, can you guess it? </span><span class="s13">42</span>

<p class="p5"><span class="s1">Nope, it’s not 42</span>

<p class="p5"><span class="s1">Your guess is too low</span>

<p class="p5"><span class="s1">I’ve picked a number between 1 and 99, can you guess it? </span><span class="s13">93</span>

<p class="p5"><span class="s1">Nope, it’s not 93</span>

<p class="p5"><span class="s1">Your guess is too high</span>

<p class="p5"><span class="s1">I’ve picked a number between 1 and 99, can you guess it? </span><span class="s13">83</span>

<p class="p5"><span class="s1">You got it!</span>

<p class="p5"><span class="s1">It took you 5 guesses.</span>

<h2><span class="s1"><b>Optional: New and Improved Deduction Game</b></span></h2>

<p class="p2"><span class="s1">Once you’ve completed the guessing game, add some usability improvements. In the line that prompts the user for input, print the <i>known range</i> the random number could be in.</span>

<p class="p2"><span class="s1">Do not increase the range if the user guesses outside your range. Example, if the current range is 40 to 60, do not change them if the user guesses 100.</span>

<p class="p2"><span class="s1">Example:</span>

<p class="p5"><span class="s1">Guess the number. 0 &lt; _ &lt; 100: </span><span class="s13">50</span>

<p class="p5"><span class="s1">Guess the number. 0 &lt; _ &lt; 50: </span><span class="s13">25</span>

<p class="p5"><span class="s1">Guess the number. 0 &lt; _ &lt; 25: </span><span class="s13">12</span>

<p class="p5"><span class="s1">Guess the number. 12 &lt; _ &lt; 25: </span><span class="s13">18</span>

<p class="p5"><span class="s1">Guess the number. 12 &lt; _ &lt; 18: </span><span class="s13">14</span>

<p class="p5"><span class="s1">Guess the number. 14 &lt; _ &lt; 18: </span><span class="s13">16</span>

<p class="p5"><span class="s1">Guess the number. 16 &lt; _ &lt; 18: </span><span class="s13">17</span>

<p class="p5"><span class="s1">Congrats you guessed it in 7 tries</span>

<p class="p2"><span class="s1"><b>Super bonus</b>: What’s the fewest number of guesses you have to make for <b>any</b> range of numbers? <i>Hint</i>: This is a <i>search algorithm</i> called a <b>binary search</b>.</span>