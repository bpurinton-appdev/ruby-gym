# Ruby Practice

 1. Open a file (e.g. `character_types.rb`) in the editor window.
 1. Modify the file per the instructions on top.
 1. Run your Ruby file by typing `ruby ` and then the name of the file you want to run in the terminal. If we want to run `character_types.rb`, we can write the command:

      ```bash
      ruby character_types.rb
      ```
   
      Remember, if there are multiple files with similar names, start typing the name and then just press <kbd>Tab</kbd> on your keyboard to let the terminal complete the name. You rarely need to type full filenames out — use **tab completion**!

1. To re-run this command, you can use the <kbd>Up ↑</kbd> and <kbd>Down ↓</kbd> arrow keys to look at the history of commands you've run in a terminal.
1. When you think you have the required output, run `rails grade` and proceed when the test passes without errors.

If you are struggling, **try to experiment directly in the IRB environment** by typing `irb` into the terminal and pressing enter. This will start an interactive Ruby terminal, where you can enter individual lines of Ruby to see their output. If you start `irb` then the terminal will no longer be in the `bash` environment so things like `rails grade` won't work. You will need to open a second terminal with the plus (+) icon and switch between the `irb` and `bash` terminals as needed. Alternatively type `exit` at the IRB terminal prompt to return to the `bash` environment.

## Required exercises

Instructions can be found in the top of the file for each.

- black_jack
- count_the
- secret_encoder
- secret_decoder
- two_fer
- character_types
- dice_roll
- sum_odd_integers
- leap_year
- raindrops
- think_fast
- accumulate


## Extra Exercises

Instructions can be found below and in file headings.

### anagram.rb

Anagram - a word, phrase, or name formed by rearranging the letters of another.
 For example, cinema is an anagram of iceman. 

Your job is to write a program that receives two words from the user separated by a comma.
 Your program should print "true" if the words are anagrams of each other and "false" if they are not. 

Example:
```bash
"Enter two words separated by a comma"
cinema,iceman
true
```

### isogram.rb

Determine if a word or phrase is an isogram.

An isogram (also known as a "nonpattern word") is a word or phrase without a repeating letter, however spaces and hyphens are allowed to appear multiple times.

Examples of isograms:

lumberjacks
background
downstream
six-year-old

The word isograms, however, is not an isogram, because the s repeats.

Your Job
Define a class called String with a class method called isogram? that accepts one String argument, and returns true or false.

Example

```ruby
String.isogram?("eleven") # => false
String.isogram?("subdermatoglyphic") # => true
```

### hamming.rb

Calculate the Hamming difference between two DNA strands.

A mutation is simply a mistake that occurs during the creation or copying of a nucleic acid, in particular DNA. Because nucleic acids are vital to cellular functions, mutations tend to cause a ripple effect throughout the cell. Although mutations are technically mistakes, a very rare mutation may equip the cell with a beneficial attribute. In fact, the macro effects of evolution are attributable by the accumulated result of beneficial microscopic mutations over many generations.

The simplest and most common type of nucleic acid mutation is a point mutation, which replaces one base with another at a single nucleotide.

By counting the number of differences between two homologous DNA strands taken from different genomes with a common ancestor, we get a measure of the minimum number of point mutations that could have occurred on the evolutionary path between the two strands.

This is called the 'Hamming distance'.

It is found by comparing two DNA strands and counting how many of the nucleotides are different from their equivalent in the other string.

GAGCCTACTAACGGGAT
CATCGTAATGACGGCCT
^ ^ ^  ^ ^    ^^

The Hamming distance between these two DNA strands is 7.

Your Job
Define a class called `Dna` with an attribute accessor called `strand` and an instance method called `distance_between` that accepts a different instance of the `Dna` class, and returns an Integer.

Example

```ruby
g_dna = Dna.new
g_dna.strand = "G"
t_dna = Dna.new
t_dna.strand = "T"

p g_dna.distance_between(t_dna) # => 1
```


### darts

Write a program that prints the earned points of a single toss of a Darts game.

Darts is a game where players throw darts to a target.

In our particular instance of the game, the target rewards with 4 different amounts of points,
 depending on where the dart lands.

If the dart lands:  
outside the target: 0 points.  
in the outer circle of the target: 1 point.  
in the middle circle of the target: 5 points.  
in the inner circle of the target: 10 points.  
 
 The outer circle has a radius of 10 units
   (this is equivalent to the total radius for the entire target),
   the middle circle a radius of 5 units, and the inner circle a radius of 1 unit.
   They are all centered to the same point (that is, the circles are concentric) defined by the coordinates (0, 0).

Write a program that asks for a point in the target
 (defined by its real Cartesian coordinates x and y),
 prints the correct amount earned by a dart landing in that point.

Example
```bash
"Enter X,Y coordinates in the format 'X,Y'"
10,10
0 points
```

Hint: the formula to find a circle with the center point (j, k) and radius (r):
   (x-j)^2 + (y-k)^2 = r^2


### phrase.rb
 
Most commonly, we define classes to represent things; those things have attributes; and we define instance methods to operate on those attributes and return useful values.

Phrase
Convert a phrase to its acronym.

Techies love their TLA (Three Letter Acronyms)!

Help generate some jargon by writing a program that converts a long name like Portable Network Graphics to its acronym (PNG).
 
Your Job
Define a class called `Phrase` with:

An attribute accessor called `body` which will store a String.
An instance method called `abbreviate` that will return a String: the uppercase first letter of each word in the phrase.

Examples
```ruby
a = Phrase.new
a.body = "Portable Network Graphics"
a.abbreviate # => "PNG"

b = Phrase.new
b.body = "Complementary metal-oxide semiconductor"
b.abbreviate # => "CMOS"
```

## Specs
<details>
  <summary>Click here to see names of each test</summary>

black_jack.rb prints "20" when the user enters '10 10' 

black_jack.rb prints "14" when the user enters '13 11' 

black_jack.rb prints "0" when the user enters '13 13' 

black_jack.rb prints "12" when the user enters '11 11' 

count_the.rb prints "'the' appeared 5 times" when the user enters 'the cabbage, the bagel, the apple, the drink, the bread' 

count_the.rb prints 'the' appeared 3 times' when the user enters 'the, beginnning the end and the middle' 

count_the.rb prints 'the' appeared 2 times' when the user enters 'the- then, the 

secret_encoder.rb should print '3 n22d t4 b2 m4r2 s2cr2t', when the input is 'I need to be more secret' 

secret_encoder.rb should print 'D4n't t2ll 1ny4n2 45r c4d2' when the input is 'Don't tell anyone our code' 

secret_decoder.rb prints 'I need to be more secret', when the input is '3 n22d t4 b2 m4r2 s2cr2t' 

secret_decoder.rb prints 'Don't tell anyone our code', when the input is 'D4n't t2ll 1ny4n2 45r c4d2' 

two_fer.rb prints 'One for Alice, one for me!' if the user enters 'alice' 

two_fer.rb prints 'One for Shreya, one for me!' if the user enters 'shreya' 

two_fer.rb prints 'One for you, one for me!' if the user enters nothing 

character_types.rb finds 8 letters, 3 spaces, and 4 digits when the user enters 'here 12 plus 25' 

character_types.rb finds 4 letters, 5 spaces, and 7 digits when the user enters 'game 1 12 58 09 ' 

character_types.rb finds 0 letters, 0 spaces, and 0 digits when the user enters '' 

dice_roll.rb prints 'You guessed correctly' when the user enters a correct guess 

dice_roll.rb prints 'Shame on you' when the user enters an incorrect guess 

sum_odd_integers.rb prints "14" when the user enters '9 5 4' 

sum_odd_integers.rb prints "0" when the user enters '2 4 6 8' 

sum_odd_integers.rb prints "5" when the user enters '1 1 3' 

leap_year.rb prints '2016 is a leap year!' if the user enters '2016' 

leap_year.rb prints '1804 is a leap year!' if the user enters '1804' 

leap_year.rb prints '1800 is not a leap year.' if the user enters '1800' 

leap_year.rb prints '2200 is not a leap year.' if the user enters '2200' 

raindrops.rb should print '52' when the input is '52' 

raindrops.rb should print 'PlingPlangPlong' when the input is '105' 

raindrops.rb should print 'Plang' when the input is '3125' 

raindrops.rb should print 'Plong' when the input is '49' 

raindrops.rb should print 'PlangPlong' when the input is '35' 

raindrops.rb should print 'Plang' when the input is '25' 

raindrops.rb should print 'PlingPlong' when the input is '21' 

raindrops.rb should print 'PlingPlang' when the input is '15' 

think_fast.rb prints '5 is odd' when when the random number is '5' 

think_fast.rb prints '40 is even' when the random number is '40' 

think_fast.rb prints 'you may pass' when `some_random_input` is 'true' 

think_fast.rb prints 'you may not pass' when `some_random_input` is 'false' 

think_fast.rb prints '[:city, :state, :zip]' when `some_random_input` is a Hash 

think_fast.rb prints 'hello!' when `some_random_input` is a 'Hello! 

think_fast.rb prints ':goodbye' when `some_random_input` is a ':GOODBYE 

think_fast.rb prints 'monday' when `some_random_input` is a Time and the current day is a Monday 

accumulate.rb prints 'Are we there yet?' 5 times when the user enters 'yes' after 4 other tries'

accumulate.rb prints an Array of the words the user entered, '["no", "no", "no", "no", "yes"]' 

accumulate.rb prints an Array of the words the user entered, '["no", "no", "123", "yeah", "yes"]' 

anagram.rb prints "false" when the user enters 'hello,olmec' 

anagram.rb prints "true" when the user enters 'elvis,lives' 

anagram.rb prints "true" when the user enters 'anagram,nag a ram' 

isogram.rb String.isogram?('angola') should return false 

isogram.rb String.isogram?('accentor') should return false 

isogram.rb String.isogram?('Emily Jung Schwartzkopf') should return true 

isogram.rb String.isogram?('six-year-old') should return 'true' 

isogram.rb String.isogram?('thumbscrew-jappingly') should return 'false' 

isogram.rb String.isogram?('thumbscrew-japingly') should return 'true' 

isogram.rb String.isogram?('alphAbet') should return false 

isogram.rb String.isogram?('eleven') should return false 

isogram.rb String.isogram?('isogram') should return true 

isogram.rb String.isogram?('') should return true 

hamming.rb the distance_between 'GGACGGATTCTG' and 'AGGACGGATTCT' should return 9 

hamming.rb the distance_between 'GGACTGAAATCTG' and 'GGACTGAAATCTG' should return 0 

hamming.rb the distance_between 'G' and 'T' should return 1 

hamming.rb the distance_between '' and '' should return 0 

darts.rb prints '1 points' when the user enters '0,10 

darts.rb prints '0 points' when the user enters '-9,9 

darts.rb prints '5 points' when the user enters '-5,0 

darts.rb prints '5 points' when the user enters '0.8,-0.8 

darts.rb prints '10 points' when the user enters '0,-1 

darts.rb prints '10 points' when the user enters '0,0 

phrase.rb has a class called 'Phrase' 

phrase.rb Phrase class has an attribute called 'body' 

phrase.rb has an instance method called, 'abbreviate', that returns the abbreviation of the Phrase's body 

phrase.rb returns 'SIMUFTA' when Phrase body is 'Something - I made up from thin air' 

phrase.rb returns 'ROTFLSHTMDCOALM' when Phrase body is 'Rolling On The Floor Laughing So Hard That My Dogs Came Over And Licked Me' 

phrase.rb returns 'CMOS' when Phrase body is 'Complementary metal-oxide semiconductor' 

phrase.rb returns 'GIMP' when Phrase body is 'GNU Image Manipulation Program' 

phrase.rb returns 'FIFO' when Phrase body is 'First In, First Out' 

phrase.rb returns 'ROR' when Phrase body is 'Ruby on Rails' 

phrase.rb returns 'PNG' when Phrase body is 'Portable Network Graphics' 

</details>
