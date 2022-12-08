# Homework overview
+ The goal of this homework is to provide a strategy to the following game : you play a game where a word is randomly chosen from a dictionary of 10-letter words, and you then try to guess what that word is. Every time you give a guess, you
are told how many characters are in common between your guess and the chosen word. The payout of the game starts at 10. If the guess is not right then the payout of the game is reduced by 1; game ends if it reaches zero or if your strategy guessed the right word.

## A first approach 
+ My first approach was :
+ 1 - Initialises a list of potential words with the whole word universe
+ 2 - pick a random word from the list of potential words and compute its distance from the secret word. Here the distance is meant as the number of common words between the guess and the secret word.
+ 3 - update the potential words lists by only keeping the words at the same distance as our current guess.
+ We repeat step 2 & 3 until we guess the secret word or we run out of guesses.

	`code let's get the win`