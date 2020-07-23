# This is a header for the application
# You should read this header and insert your name and your date below as part of the peer review
# This is a typical part of any program
# Author: <author>
# Creation Date: <date>
# Below is a simple program with 10 issues (some are syntax errors and some are logic errors.  You need to identify the issues and correct them.

import random
import time

def displayIntro():
	print('''You are in a land full of dragons. In front of you,
	you see two caves. In one cave, the dragon is friendly
	and will share his treasure with you. The other dragon
	is greedy and hungry, and will eat you on sight.''')
	print()

def chooseCave():
    cave = ''
    #while cave != '1' and cave != '2':
    while cave != '1' and cave != '2':
	# 1) While statement TabError: inconsistent use of tabs and spaces in indentation
		
		#print('Which cave will you go into? (1 or 2)')
    	print('Which cave will you go into? (1 or 2)')
    	## 3) cave = input TabError: inconsistent use of tabs and spaces in indentation

		#cave = input()
    	cave = input()
		# 3) cave = input TabError: inconsistent use of tabs and spaces in indentation
    
	#return caves
    return cave
	# 4) return caves TabError: inconsistent use of tabs and spaces in indentation
	# 5) caves should be cave

def checkCave(chosenCave):
	print('You approach the cave...')
	#sleep for 2 seconds
	time.sleep(2)
	print('It is dark and spooky...')
	#sleep for 2 seconds
	time.sleep(3)
	print('A large dragon jumps out in front of you! He opens his jaws and...')
	print()
	#sleep for 2 seconds
	time.sleep(2)
	friendlyCave = random.randint(1, 2)

	if chosenCave == str(friendlyCave):
		print('Gives you his treasure!')
	else:
		#print 'Gobbles you down in one bite!'
		print('Gobbles you down in one bite!')
		# 6) Missing parentheses

playAgain = 'yes'

#while playAgain = 'yes' or playAgain = 'y':
while playAgain == 'yes' or playAgain == 'y':
# 7 and 8) Invalid syntax in while statement == not =

	displayIntro()

	#caveNumber = choosecave()
	caveNumber = chooseCave()
	# 9) Should be chooseCave() not choosecave()

	checkCave(caveNumber)
    
	print('Do you want to play again? (yes or no)')
	playAgain = input()

	#if playAgain == "no":
	if playAgain == 'no' or playAgain == 'n':
	# 10) Added "or playAgain == 'n'" also, changed "no" to 'no' for consistency

		#print("Thanks for planing")
		print ('Thanks for playing')
		# 11) Typo: playing instead of planing and single quotes for consistency
		
	else:
		print('Do you want to play again? (yes or no)')
		playAgain = input()
	# 12) Adding else statement to ask again when yes, y, no, or n is not entered.
	# Otherwise the program exits and user doesn't get the thank you message.
