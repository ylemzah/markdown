# Homework overview
+ The goal of this homework is to provide a strategy to the following game : you play a game where a word is randomly chosen from a dictionary of 10-letter words, and you then try to guess what that word is. Every time you give a guess, you
are told how many characters are in common between your guess and the chosen word. The payout of the game starts at 10. If the guess is not right then the payout of the game is reduced by 1; game ends if it reaches zero or if your strategy guessed the right word.

## A first approach 
+ My first approach was :
+ 1_ Initialises a list of potential words with the whole word universe
+ 2_ pick a random word from the list of potential words and compute its score from the secret word. Here the score is meant as the number of common words between the guess and the secret word.
+ 3_ update the potential words lists by only keeping the words at the same distance as our current guess.
+ We repeat step 2 & 3 until we guess the secret word or we run out of guesses.

A pseudo code for this algorithm would be :

```
>potential_list = words_universe
>attempts <- 10
>score <-0
>while attempts > 0 do

>>    guess random word from potential_list    
>>   score <- score(word,secret_word)  
>>    if score = 10 do 
>>>       break  
>>    else do  
>>>      potential_list <- words such that score(words,guess)=score 
>>>      attempts <- attempts - 1
``` 

>while not convergence:
>
>> compute $\nabla(J)$
>>
>> $\theta_0 := \theta_0 - \alpha\nabla(J)_0$
>>
>> $\theta_1 := \theta_1 - \alpha\nabla(J)_1$
>
>end while




