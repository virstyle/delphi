# Bowling

Score a bowling game.

Bowling is a game where players roll a heavy ball to knock down pins
arranged in a triangle. Write code to keep track of the score
of a game of bowling.

## Scoring Bowling

The game consists of 10 frames. A frame is composed of one or two ball
throws with 10 pins standing at frame initialization. There are three
cases for the tabulation of a frame.

* An open frame is where a score of less than 10 is recorded for the
  frame. In this case the score for the frame is the number of pins
  knocked down.

* A spare is where all ten pins are knocked down by the second
  throw. The total value of a spare is 10 plus the number of pins
  knocked down in their next throw.

* A strike is where all ten pins are knocked down by the first
  throw. The total value of a strike is 10 plus the number of pins
  knocked down in the next two throws. If a strike is immediately
  followed by a second strike, then the value of the first strike
  cannot be determined until the ball is thrown one more time.

Here is a three frame example:

| Frame 1         | Frame 2       | Frame 3                |
| :-------------: |:-------------:| :---------------------:|
| X (strike)      | 5/ (spare)    | 9 0 (open frame)       |

Frame 1 is (10 + 5 + 5) = 20

Frame 2 is (5 + 5 + 9) = 19

Frame 3 is (9 + 0) = 9

This means the current running total is 48.

The tenth frame in the game is a special case. If someone throws a
strike or a spare then they get a fill ball. Fill balls exist to
calculate the total of the 10th frame. Scoring a strike or spare on
the fill ball does not give the player more fill balls. The total
value of the 10th frame is the total number of pins knocked down.

For a tenth frame of X1/ (strike and a spare), the total value is 20.

For a tenth frame of XXX (three strikes), the total value is 30.

## Requirements

Write code to keep track of the score of a game of bowling. It should
support two operations:

* `roll(pins : int)` is called each time the player rolls a ball.  The
  argument is the number of pins knocked down.
* `score() : int` is called only at the very end of the game.  It
  returns the total score for that game.

## Testing

In order to run the tests for this track, you will need to install
DUnitX. Please see the [installation](http://www.exercism.io/languages/delphi/installing) instructions for more information.

### Loading Exercises into Delphi

If Delphi is properly installed, and `*.dpr` file types have been associated with Delphi, then double clicking the supplied `*.dpr` file will start Delphi and load the exercise/project.  `control + F9` is the keyboard shortcut to compile the project or pressing `F9` will compile and run the project.

Alternatively you may opt to start Delphi and load your project via. the `File` drop down menu.

### When Questions Come Up
We monitor the [Pascal-Delphi](https://gitter.im/exercism/Pascal-Delphi) support room on [gitter.im](https://gitter.im) to help you with any questions that might arise.

### Submitting Exercises

Note that, when trying to submit an exercise, make sure the exercise file you're submitting is in the `exercism/delphi/<exerciseName>` directory.

For example, if you're submitting `ubob.pas` for the Bob exercise, the submit command would be something like `exercism submit <path_to_exercism_dir>/delphi/bob/ubob.pas`.

## Source

The Bowling Game Kata at but UncleBob [http://butunclebob.com/ArticleS.UncleBob.TheBowlingGameKata](http://butunclebob.com/ArticleS.UncleBob.TheBowlingGameKata)

## Submitting Incomplete Solutions
It's possible to submit an incomplete solution so you can see how others have completed the exercise.
