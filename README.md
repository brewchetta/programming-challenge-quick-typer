# Pair Programming Challenge - Quick Typer

The purpose of this challenge is to build a game that challenges users to type as many words as they can before the timer expires. This game makes heavy use of Javascript to present the user with a clock, check what they're inputting, and score them based on the words they've typed.

## Getting Started

Fork and then clone down the repository. Open up the code and also use a browser to see what the `index.html` looks like.

Take some time to understand the code that's already written. If you need to, change the different variables to see what happens with them. There are notes in the code that should explain what different sections are meant to be.

## Current Word Input

When looking at the `typer-input` field (which gets set to hidden when the script runs) we want to make it so that whenever its value matches the current word, we add that word to the user's "score" in `completed-words` and display a new word for the user to type in `word-display`.

Comment out the line that makes the `typer-input` hidden. You'll notice there's already an event listener attached to it which fires whenever we type something in. You can utilize this to check and see if the input matches the current word.

Whenever the input matches, you'll want to do a few things:

- Add the word to the `completed-words` list

- Change the current word with the `newWord` function

- Clear the `typer-input` value

- Change the `word-input` to display the new word

Be sure to comment back in the code that initially hides the `typer-input` after you're satisfied that everything's working properly.

## Starting the Timer

To make the game function properly, you'll need to build out a timer that counts down to zero. While the timer runs, the user is able to type words, however when it reaches zero the game ends.

The `countdown-button` already has an event listener attached to it. When the button is clicked, hide the button and make the countdown clock visible. Set the countdown clock to display 20 (the number of seconds our user has to type as many words as they can).

Additionally, you'll want to start the countdown with an interval using `setInterval` (be sure to look it up if you're shaky on the syntax!). For every second that passes, lower the count by one / display the updated count to the user.

When the interval reaches 0, clear the interval (or else it'll keep going ticking in the background!). Make the `countdown-button` visible again and the `typer-input` hidden. This way the user can't type anything else in but they're able to see all the words they've typed out!

## Additional details

There are a few other optimizations we can make. The first is we can make it so the user immediately gets focused on the `typer-input` field when the `countdown-button` gets clicked. Look up how to focus an input if you're unsure how to do that!

Additionally, when we click the button we should clear out the `completed-words` list so the user starts fresh every time.

Beyond that, what other fun features or polish can you think to add?
