# The Three Card Puzzle

Suppose we have three cards in a hat:
  - RB - One card is painted blue on one side and red on the other.
  - BB - One card is painted blue on both sides.
  - RR - One card is painted red on both sides.
 
### The Setup
  - I pick one of the three cards at random, flip it to a random side, and place it on the table.
  - U  be the color of the side of the card facing up. (B or R)
  
### The Bet
  - If the other side of the card has a different I pay you $1.
  - If the other side has the same color you pay me $1.
  
### Why is this fair?
  - Suppose U is R.
  - Then the card is either RR or RB.
  - Therefor the other side can be either R or B
  - Therefor in this case the odds are equal.
  - A similar argument holds for the case where U is B
  
```
red_bck="\x1b[41m%s\x1b[0m"
blue_bck="\x1b[44m%s\x1b[0m"
red=red_bck%'R'
black=blue_bck%'B'
Cards=[(red,black),(red,red),(black,black)]
counts={'same':0,'different':0}
from random import random
for j in range(50):
    i=int(random()*3.)  # Select a random card
    side=int(random()*2.)
    C=Cards[i]
    if(side==1):        # select which side to be "up"
        C=(C[1],C[0])
    same= 'same' if C[0]==C[1] else 'different'  # count the number of times the two sides are the same or different.
    counts[same]+=1
    print(''.join(C)+' %-9s'%same,)
    if (j+1)%5==0:
        print
print()
print(counts)
```
![](/Images/t2c3.png)

### The Simulation does not agree with the argument
  - In Simulation: the two sides have the same color about twice the number of times that they have different color.
  - You are twice as likely to lose as you are to win.
  - On average you lose 33 cents per iteration.
  
### Alternative argument 

If we pick a card at random 2/3 of the time we pick a card where the two sides have the same color, and only 1/3 where the color is different.
  - The original argument also sounds convincing, but is wrong.
