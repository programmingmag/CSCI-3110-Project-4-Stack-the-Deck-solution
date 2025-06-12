# CSCI-3110-Project-4-Stack-the-Deck-solution

Download Here: [CSCI 3110 Project 4: Stack the Deck solution](https://jarviscodinghub.com/assignment/project-4-stack-the-deck-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

File(s) to be submitted: proj4.cpp, card.h, card.cpp,
deck.h, deck.cpp, player.h, player.cpp, makefile.
Above files must be uploaded individually.

Objectives:
1) Class composition/aggregation; 2) Using multiple classes; 3) Operator overloading; 4) Overloading
ostream; 5) Using friend functions; 6) Use of static variables.

Project description:
Write a C++ program to simulate a simple card game between two players. The game proceeds as follows: The 52
cards in a deck of cards are shuffled and each player draws three cards from the top of the deck. Remaining cards are
placed in a pile face-down between the two players. Players then select a card from the three in their hand. The player
playing the card with the highest point value wins, and collects both cards and adds them to their pile (score). If the
cards played have the same point value, the hand is a draw (tie) and no points are accumulated by either player.

At the
completion of a hand, each player draws the top card from the deck to add to their hand (player 1 first then player 2).

Play continues until all cards have been played. The winner is the player with the most points at game’s end.
You will use a standard deck of 52 cards where there are thirteen cards from each of four suits: hearts, spades,
diamonds, and clubs. The thirteen cards in point order are the 2-10 numbered cards, the face cards (Jack, Queen, King),

and the Ace card. Points are distributed as follows: Ace=15, face cards=10, all other cards count as their numeric value.

Requirements:
1. Your program must be split into 7 files. There will be 3 classes (each with separate interface and implementation
files), and a driver file. The requirements for these are specified below:
a) The Card class – This class represents an individual card
 Files must be named card.h and card.cpp
 Class must be named Card
 The interface (header file) is provided.

i. You should implement the interface file in a .cpp implementation file
ii. All data members must be of the type specified in the header file
iii. All member functions in the interface file must be implemented as declared – However you have
flexibility in how you choose to implement the body of each, consistent with the specifications

b) The Deck class – This class represents the deck of cards
 Files must be named deck.h and deck.cpp
 Class must be named Deck
 The interface (header file) is provided.

i. You should implement the interface file in a .cpp implementation file
ii. All data members must be of the type specified in the header file
iii. All member functions in the interface file must be implemented as declared – However you have
flexibility in how you choose to implement the body of each, consistent with the specifications

c) The Player class – This class will represent the human and computer player – Play is autonomous
 Files must be named player.h and player.cpp
 Class must be named Player
 The interface (header file) is provided.
i. You should implement the interface file in a .cpp implementation file

ii. All data members must be of the type specified in the header file
iii. All member functions in the interface file must be implemented as declared – However you have
flexibility in how you choose to implement the body of each, consistent with the specifications

c) A driver, or client, file
 Must be named proj4.cpp
 Reads an input configuration file named cardgame.txt, consisting of:
1. First line: Player 1’s name (a single word)
2. Second line: Player 2’s name (a single word)
3. Third line: A positive integer to be used as the random number seed

 Must contain the line srand(x); (where x is the seed read from the file), prior to below processing
 Must instantiate the players
 Must instantiate the card deck – The deck has 52 cards (13 per suit), in this suit order: Clubs, Hearts, Spades,

Diamonds, and card order: Ace card has face value 0, 2 card has face value 1, 3 card has face value 2, and so
on to the King card (face value 12). Order is from the bottom of the deck (Ace of Clubs → King of Diamonds).

 The deck array must be shuffled using std::random_shuffle (requires the algorithm header file be included)
– Use std::begin and std::end on the deck array to pass as iterators to this function. Do not use std::shuffle.
 Each player alternates taking a card from the top of the deck, until each has 3 cards
 Game play proceeds as follows:

1. Each player selects the highest card by point value. If multiple cards in the player’s hand have the
same point value, then face value will be used to determine the highest card. If at this stage
multiple cards have the same face value, the suit will be used to determine which card is highest, by
using the following precedence (in decreasing order): Clubs, Hearts, Spades, Diamonds.

2. The player playing the card with the highest point value wins, and collects both cards and adds them
to their pile (score). If both cards played have the same point value, the hand is a draw (tie) and no
points are accumulated by either player.

3. Player 1 will replace the card just played by drawing a card from the top of the deck. Player 2 will
then do the same, and play continues.

 Output for this program must clearly and neatly show that the program works and that it works correctly.
Your output must match the one provided.

The suits, Clubs, Hearts, Spades, and Diamonds are shown as (C,
H, S, D) respectively, immediately following the card face. Point values follow in brackets. Your code must:
1. Display the entire deck of cards after it is instantiated (before shuffling it) – Top of deck displayed first.
2. Display the shuffled deck (prior to players picking their first 3 cards) – Top of deck displayed first.

3. Players alternate drawing the card at the top of the deck – player 1 then player 2 – to (re)fill their hand
4. For each turn of play, two lines are output (see sample output)

 Pre-Play: Turn #, player name, card in each card slot of hand, and score (player 1 then player 2)
 Post-Play: Turn #, player name, card in each card slot of hand, and score (player 1 then player 2) –
The winning player’s name should be followed by an asterisk (if the turn is a draw, no winner is
identified); the slot from which the card was played should be shown as empty; the scores should
reflect the outcome of the turn of play

5. At the end of the game, output one of the following:
 The word “Winner” followed by the name of the player with the highest score, and their score
 The word “Tie”, followed by the tie score
 A sample output file of a complete game is provided. Your output must match this format exactly, as far as
spacing and content. You are not required to create this output file. It is an example for you to follow.

2. Test your program – Use different see values for random initialization.
3. Code comments – Add the following comments to your code:
 A section at the top of the source file(s) with the following identifying information:
Your Name
CSCI 3110-00X (your section #)
Project #X
Due: mm/dd/yy
 Below your name add comments in each file that give an overview of the program or class.
 Place a one or two line comment above each function that summarizes the workings of the function.

4. Rubric
Requirement Points Off
main: Input filename -3
main: Data correctly read from file -10
main: Random number seeding -5
main: Players instantiated -5
main: Deck instantiated -3
main: Deck displayed (pre-shuffle) – Top card first -5
main: Deck shuffled -10
main: Deck displayed (post-shuffle) – Top card first -5
main: Game play for each turn (play, decide winner, update scores, replenish hand) -12 (3 pts each)
main: Failure to play all turns (until all cards are gone) -15
main: Output per the specification, for each turn of play -10
main: Final game score and result output -5

Card: Types and names of variables, functions, parameters, etc. per specification -5 (each)
Card: Constructors correctly initialize objects -5
Card: Comparison operators correctly overloaded -4 (each)
Card: ostream << correctly overloaded -5
Card: getPointValue: Correct value returned -3
Deck: Types and names of variables, functions, parameters, etc. per specification -5 (each)

Deck: Constructor correctly initializes deck with cards in the order specified -5
Deck: Invokes std::random_shuffle to shuffle the deck -5
Deck: ostream << correctly overloaded -5
Deck: dealCard: Returns card at the top of the deck -5
Deck: isEmpty: Correct value returned -5
Player: Types and names of variables, functions, parameters, etc. per specification -5 (each)
Player: Constructor correctly initialize player name -5
Player: playCard: Selects the correct card to play, per the specification -10
Player: drawCard: Correctly replaces previously played card -10
Player: ostream << correctly overloaded -5
Player: addScore: Correctly adds card value to player’s score -4
Player: emptyHand: Returns true when player has no cards in hand -3
Player: getName: Returns the player’s name -3
Player: getScore: Returns the player’s score -3
general: Does not compile (on ranger using Linux g++ compiler, and the provided makefile) -25
general: Runtime crash -25
general: Other TBD



