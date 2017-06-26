# `shuffle`

An aid for randomizing a physical deck of cards.

## Usage

`shuffle UNIQUE [GROUP...]`

All non-option arguments must be integers. UNIQUE is the number of unique,
unshuffled cards. The GROUPs are numbers of identical or pre-shuffled cards.
When stacking the initial deck, arrange the cards specified by the arguments
from the top down.

The program will tell you how to divide the deck into two equal halves, called A
and B. You will see something like "2 to A", which means to put 2 cards from the
deck into pile A. Press Enter, and the program will tell you how many cards to
put into pile B, and so on. (The first instruction may start with either A or
B.) This will continue until you have distributed all of the cards from the deck
to piles A and B.

Move pile B to the right, and pick up pile A. You will repeat the same process
with the pile in your hand that you went through with the full deck. When you're
done, move pile B to the right (to the left of the original pile B), and pick up
pile A, as before.

Eventually, you will end up with one or both piles with only one card. This
single card is fully randomized. Put it to your left to start the final,
shuffled deck. If both piles have only one card, move card A to the shuffled
pile first, then card B.

Whenever you finish dividing up a pile, the next pile you divide will always be
the smallest of the unfinished piles. This will be pile A, if it has more than
one card. Otherwise, it will be the most recent unfinished B pile that you
created.

When you have moved all cards into the final deck, you're done.
