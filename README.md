# AboutMe
Biography


Hello, my name is Brittney Watson. I am currently persuing my Master's Degree in Cyber Security. I graduated with a Bachelor's of Science in Management Information Systems, from the University of Tampa. In the near future, I plan to return after completing some final courses, gain some experience, get some certificatins and then start my own business. I find graphic designing very interesting, as I have my own graphic design business. The reason I chose this field was because  despite doing well in most of my course, I prefer to deal with computers rather than people. 


See below for program:


"""
Author: <Brittney Watson>
Description: <Create a program that uses concepts from this class (be creative!)>
"""

import random
import Test2Pt2b #importng prime numbers program from another file 

WORD = ('cyber', 'security', 'rocks')
word = random.choice(WORD)
correct = word
hint = word[0] + word[(len(word)-1):(len(word))]
letter_guess = ''
word_guess = ''
store_letter = ''
count = 0
limit = 3

print('Welcome to the guess the word game!"')
print('You have 3 attempts at guessing the letters in a word')
print('Start!')

while count < limit:
    letter_guess = input('Guess the letter: ')

    if letter_guess in word:
        print('yes!')
        store_letter += letter_guess
        count += 1

    if letter_guess not in word:
        print('Sorry try again!')
        count += 1

    if count == 2:
        print('\n')
        hintRequest = input('Would you like a hint? ')
        if hintRequest == 'y':
            print('\n')
            print('HINT: The first and last letter of the word is: ', hint)
        if hintRequest == 'n':
            print('You are brave!')

print('\n')
print('So far you have guessed ',len(store_letter),'letters correctly.')
print('These letters are: ', store_letter)

word_guess = input('Guess the word: ')
while word_guess:
    if word_guess.lower() == correct:
        print('Awesome!')
        break

    elif word_guess.lower() != correct:
        print('Sorry! The answer was,', word)
        break

print('\n')

#Round two 
print('Wait! One more guess before you go :) ')

G1 = input ('Is 7 a prime number?: ')

if G1 == 'yes': 
    answer = Test2Pt2b.checkIfPrime(13) 
    print (answer)
else: 
    print ('False')

print('Thanks for playing the guessing game!')
