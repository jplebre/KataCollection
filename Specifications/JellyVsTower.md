# Jelly vs Tower

## Description
Based on a board game, similar to the JellyDefense mobile game.
Towers are setup in a map defend a town against incoming jellies.
Create a console application (or GUI if you are up for it).
Damaged is related to tower and jelly level, as well as their colour.

* Ensure jellies and towers can be of different colours: **Blue**, **Red**, **RedBlue**.
* Jellies and Towers should have a health and be alive or dead.
* Provide a way to identify each individual tower and Jelly.

  ```
  Blue Red Tower 1 : Level 1 
  Blue Tower 1 : Level 2 
  Blue Tower 2 : Level 4
  Red Tower 1 : Level 1
  ```
  
* Implement a game script that creates towers and Jellies and outputs something like:
  ```
  Blue Red Tower attacks Jelly for 1 point damage. 
  Blue Tower attacks Jelly for 2 points damage. 
  Blue Tower attacks Jelly for 2 points damage. 
  Red Tower attacks Jelly for 2 points damage.
  ```

* Make sure the following rules apply:<br>

  | Tower Type   |          Blue Jelly          |           Red Jelly           |
  |--------------|------------------------------|-------------------------------|
  | ￼Blue Tower   | Level 1: 2-5 points damage   | Level 1: 0 points damage      | 
  |              | Level 2: 5-9 points damage   | Level 2: 1 points damage      |
  |              | Level 3: 9-12 points damage  | Level 3: 2 points damage      |
  |              | Level 4: 12-15 points damage | Level 4: 3 points damage      |
  | Red Tower    | Level 1: 0 points damage     | Level 1: 2-5 points damage    |
  |              | Level 2: 1 points damage     | Level 2: 5-9 points damage    |
  |              | Level 3: 2 points damage     | Level 3: 9-12 points damage   |
  |              | Level 4: 3 points damage     | Level 4: 12-15 points damage  |
  ￼| BlueRedTower | Level 1: 2 points damage     | Level 1: 2 points damage      |
  |              | Level 2: 2-4 points damage   | Level 2: 2-4 points damage    |
  |              | Level 3: 4-6 points damage   | Level 3: 4-6 points damage    |
  |              | Level 4: 6-8 points damage   | Level 4: 6-8 points damage    |
