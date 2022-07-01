# Problem Set 1: Coins

<!-- ![Coins](/assets/images/coins.jpg "25 cents, 10 cents, 5 cents, 1 cent") -->
<img src="{{ '/assets/images/coins.jpg' | relative_url }}" alt="25 cents, 10 cents, 5 cents, 1 cent" title="25 cents, 10 cents, 5 cents, 1 cent">


## Background

When making change, odds are you want to minimize the number of coins you’re dispensing for each customer, lest you run out (or annoy the customer!). Fortunately, computer science has given cashiers everywhere ways to minimize numbers of coins due: **greedy algorithms**.

A greedy algorithm takes the best solution at that time.

Where might have you used a greedy algorithm?

Suppose that a cashier owes a customer some change and in that cashier’s drawer are quarters (25¢), dimes (10¢), nickels (5¢), and pennies (1¢). The problem to be solved is to decide which coins and how many of each to hand to the customer. Think of a "greedy" cashier as one who wants to take the biggest bite out of this problem as possible with each coin they take out of the drawer. For instance, if some customer is owed 41¢, the biggest first bite that can be taken is 25¢. (That bite is “best” inasmuch as it gets us closer to 0¢ faster than any other coin would.) Note that a bite of this size would whittle what was a 41¢ problem down to a 16¢ problem, since 41 - 25 = 16. That is, the remainder is a _similar but smaller_ problem. Needless to say, another 25¢ bite would be too big, and so our greedy cashier would move on to a bite of size 10¢, leaving him or her with a 6¢ problem. At that point, greed calls for one 5¢ bite followed by one 1¢ bite, at which point the problem is solved. The customer receives one quarter, one dime, one nickel, and one penny: four coins in total. As long as a cashier has enough of each coin, this largest-to-smallest approach will yield the fewest coins possible!

## Implementation Guide

* I've already written the code to prompt the user for a dollar amount of change. I've also written the code segment to convert dollars to cents.
	* What happens if the user inputs a negative dollar amount? Or a word? Modify the code to handle those _edge cases_.
* Your code should print out the minimum number of coins need to make the change:
    ```
	> Change owed: $0.41
	4
    ```
* Your program should behave like
    ```
	> Change owed: -0.41
	> Change owed: foobar
	> Change owed: 0.41
	4
    ```

## Hints

Does your program work when you input
* `-1.00`, or any other negative number?
* `0.00`?
* `1.00`, or any other positive number?
* letters or words?
* no input at all, when you only hit Enter?