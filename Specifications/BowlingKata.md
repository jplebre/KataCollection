# Bowling Kata

Simulate a bowling game.

## Background Info

Create a program, which, given a valid sequence of rolls for one line of American Ten-Pin Bowling, produces the total score for the game.
Here are some things that the program will not do:

We will not check for valid rolls.
We will not check for correct number of rolls and frames.
We will not provide scores for intermediate frames.


## Specification

We can briefly summarize the scoring for this form of bowling:

Each game, or “line” of bowling, includes ten turns, or “frames” for the bowler.
In each frame, the bowler gets up to two tries to knock down all the pins.
If in two tries, the bowler fails to knock them all down, the score for that frame is the total number of pins knocked down in those two tries.
If in two tries the bowler knocks them all down, this is called a “spare” and the score for the frame is ten plus the number of pins knocked down on the next throw (in the next turn).
If on their first try in the frame the bowler knocks down all the pins, this is called a “strike”. The turn is over, and the score for the frame is ten plus the simple total of the pins knocked down in the next two throws.
If the bowler gets a spare or strike in the last (tenth) frame, the bowler gets to throw one or two more bonus balls, respectively. These bonus throws are taken as part of the same turn. If the bonus throws knock down all the pins, the process does not repeat: the bonus throws are only used to calculate the score of the final frame.
The game score is the total of all frame scores.

More info on the rules at: [How to Score for Bowling](http://www.topendsports.com/sport/tenpin/scoring.htm)

### Tips

What makes this game interesting to score is the lookahead in the scoring for strike and spare. At the time we throw a strike or spare, we cannot calculate the frame score: we have to wait one or two frames to find out what the bonus is.


## Use Case Scenarios


## Test Data

(When scoring “X” indicates a strike, “/” indicates a spare, “-” indicates a miss)

  * X X X X X X X X X X X X (12 rolls: 12 strikes) = 10 frames * 30 points = 300
  * 9- 9- 9- 9- 9- 9- 9- 9- 9- 9- (20 rolls: 10 pairs of 9 and miss) = 10 frames * 9 points = 90
  * 5/ 5/ 5/ 5/ 5/ 5/ 5/ 5/ 5/ 5/5 (21 rolls: 10 pairs of 5 and spare, with a final 5) = 10 frames * 15 points = 150

## Credits

http://codingdojo.org/kata/Bowling/