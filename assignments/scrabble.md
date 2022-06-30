# Lab 2: Scrabble

## Background

In the game of [Scrabble](https://scrabble.hasbro.com/en-us/rules), players create words to score points, and the number of points is the sum of the point values of each letter in the word.

| **A** | **B** | **C** | **D** | **E** | **F** | **G** | **H** | **I** | **J** | **K** | **L** | **M** | **N** | **O** | **P** | **Q** | **R** | **S** | **T** | **U** | **V** | **W** | **X** | **Y** | **Z** |
|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|
| 1     | 3     | 3     | 2     | 1     | 4     | 2     | 4     | 1     | 8     | 5     | 1     | 3     | 1     | 1     | 3     | 10    | 1     | 1     | 1     | 1     | 4     | 4     | 8     | 4     | 10    |

For example, if we wanted to score the word `Code`, we would note that in general Scrabble rules, the `C` is worth 3 points, the `o` is worth 1 point, the `d` is worth 2 points, and the `e` is worth 1 point. Summing these, we get `Code` is worth `3 + 1 + 2 + 1 = 7` points.

## Getting Started

* Head over to [Scrabble (Lab 2) in Replit](https://replit.com/team/ap-csp0)

## Implementation Guide

Complete the implementation of `scrabble.py` such that it determines the winner of a short scrabble-like game, where two players each enter their word and the high scoring player wins.

* Notice that we've stored point values of each letter of the alphabet in a list named `POINTS`.
    * For example, `A` or `a` is worth 1 point (represented by `POINTS[0]`), `B` or `b` is worth 3 points (represented by `POINTS[1]`), etc.
* In `main()`, the program prompts the two players for their words using `input()`. These values are stored inside variables named `word1` and `word2`.
* In `computeScore()`, your program should should compute, using the `POINTS` list, and return the score for the input. Characters that are not letters should be given zero points, and uppercase and lowercase letters should be given the same point values.
    * For example, `!` is worth `0` points while `A` and `a` are both worth `1` point.
    * Though Scrabble rules normally require that a word be in the dictionary, no need to check for that in this problem!
* In `main()`, your program should print, depending on the players' scores, `Player 1 wins!`, `Player 2 wins!`, or `Tie!`.

## Hints

* You may find the functions `isupper()` and `islower()` to be helpful to you. These functions return `True` if all the characters in the string are uppercase (for `isupper`) or lowercase (for `islower`).
    * Example: `HELLO.isupper()` returns `True` while `HELLO.islower()` returns `False`.
* Likewise, `upper()` and `lower()` returns returns a string that is all uppercase (for `upper`) or lowercase (for `lower`).
    * Example: `hello.upper()` returns `HELLO` while `HELLO.lower()` returns `hello`.
* To find the value at the `n`th index of a list called `my_list`, we can write `my_list[n]`. We can apply this to strings as well, as strings are arrays of characters.
* Recall that computers represent characters using [ASCII](http://asciitable.com/), a standard that represents each character as a number.