# Problem Set 3: Plurality

## Background

Elections come in all shapes and sizes. In the UK, the [Prime Minister](https://www.parliament.uk/education/about-your-parliament/general-elections/) is officially appointed by the monarch, who generally chooses the leader of the political party that wins the most seats in the House of Commons. The United States uses a multi-step [Electoral College](https://www.archives.gov/federal-register/electoral-college/about.html) process where citizens vote on how each state should allocate Electors who then elect the President.

Perhaps the simplest way to hold an election, though, is via a method commonly known as the "plurality vote" (also known as "first-past-the-post" or "winner take all"). In the plurality vote, every voter gets to vote for one candidate. At the end of the election, whichever candidate has the greatest number of votes is declared the winner of the election.

## Getting Started

## Understanding

Let's now take a look at `plurality.py` and read through the starter code that's been provided to you.

The file then defines a dictionary called a candidate. Each candidate in the dictionary is represented by a key representing the candidate’s name and a value representing the number of votes the candidate has. Example: `candidates["Forrest"] = 7, candidates["Jenny"] = 1`

Now, take a look at the `main` function itself. That `while` loops repeatedly asks for the names of the candidates in the election, until the user presses Enter. Then the program asks the user to type in the number of voters; this value is stored in `voter_count`. Then, the program lets every voter type in a vote (see how?), calling the vote function on each candidate voted for. Finally, `main` makes a call to the printWinner function to print out the winner (or winners) of the election.

If you look further down in the file, though, you'll notice that the `vote` and `printWinner` functions have been left blank. This part is up to you to complete!

## Implementation Guide

Complete the implementation of `plurality.py` in such a way that the program simulates a plurality vote election.
* Complete the `vote` function.
    * `vote` takes in a single argument, a string called `name`, that represents the name of the candidate who was voted for.
    * If `name` matches one of the names of the candidates in the election, then update that candidate's vote total to account for the new vote. The `vote` function should return `True` to indicate a successful ballot.
    * If `name` does not match the name of any of the candidates in the election, no vote totals should change, and the `vote` functions should return `False` to indicate an invalid ballot.
    * You may assume that no two candidates will have the same name.
* Complete the `printWinner` function:
    * The function should print out the name of the candidate who received the most votes in the election, and then print a newline.
    * It is possible that the election could end in a tie if multiple candidates each habe the maximum number of votes. In that case, you should output the names of each winning candidates, each on a separate line.