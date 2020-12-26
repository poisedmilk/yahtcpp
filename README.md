# yatch-cpp

C++ Implementation of the popular game yahtzee. 

The following skills are being practiced in the development of this game:

- C++ Classes
- Doxygen Automatic Documentation Generation
- UI/UX (Game TUI in command line)
- Elementary Implementation of an AI (CPU Player)

## How to Play (Game Rules)

Yahtzee is played by rolling five dice when it is a users turn. After rolling, the user must fill out one of the available score boxes on his/her score sheet. It is advantageous of the user to pick a selection that provides him/her the highest score for that round, but its also the nature of the game Yahtzee to weigh the risks and benefits of taking a hit early on to increase your chances of rolling dice that provide you a higher score for a specific section later on in the game. Each turn, the user is allowed to re-roll his/her dice 3 times. During each re-roll, the user may choose to roll all 5 of the die or hold any number of the die and only roll the other die. 

### Score Card

Below is the score card describing how the score is tallied for each round and how the Grand Total is calculated at the end of the game. The score card is broken up into an upper section and a lower section but both sections may be filled out at any point during the game. 



#### Upper Section

| UPPER SECTION                    | HOW TO SCORE            | GAME #1 | GAME #2 | GAME #3 | GAME #4 | [...] | GAME #13 |
| -------------------------------- | ----------------------- | ------- | ------- | ------- | ------- | ----- | -------- |
| Aces (⚀ = 1)                     | 1 pt per Ace in hand    |         |         |         |         |       |          |
| Twos (⚁ = 2)                     | 2 pts per Two in hand   |         |         |         |         |       |          |
| Threes (⚂ = 3)                   | 3 pts per Three in hand |         |         |         |         |       |          |
| Fours (⚃ = 4)                    | 4 pts ber Four in hand  |         |         |         |         |       |          |
| Fives (⚄ = 5)                    | 5 pts per Five in hand  |         |         |         |         |       |          |
| Sixes (⚅ = 6)                    | 6 pts per Six in hand   |         |         |         |         |       |          |
| **Total Score**                  | **---------------->**   |         |         |         |         |       |          |
| BONUS if total score above >= 63 | 35 pts                  |         |         |         |         |       |          |
| **Total of Upper Section**       | **---------------->**   |         |         |         |         |       |          |

#### Lower Section

| LOWER SECTION               | HOW TO SCORE          | GAME #1 | GAME #2 | GAME #3 | GAME #4 | [...] | GAME #13 |
| --------------------------- | --------------------- | ------- | ------- | ------- | ------- | ----- | -------- |
| 3 of a kind                 | Add Total of All Dice |         |         |         |         |       |          |
| 4 of a kind                 | Add Total of All Die  |         |         |         |         |       |          |
| Full House                  | Score 25              |         |         |         |         |       |          |
| Sm Straight (Sequence of 4) | Score 30              |         |         |         |         |       |          |
| Lg Straight (Sequence of 5) | Score 40              |         |         |         |         |       |          |
| YAHTZEE (5 of a kind)       | Score 50              |         |         |         |         |       |          |
| Chance                      | Sum of all 5 Die      |         |         |         |         |       |          |
| Total of Lower Section      | **---------------->** |         |         |         |         |       |          |
| Total of Upper Section      | **---------------->** |         |         |         |         |       |          |
| **GRAND TOTAL**             | **---------------->** |         |         |         |         |       |          |

### Winning

The winner is determined once all turns are complete, and each box on the Yahtzee score card has been filled in for all players. The scorecard is tallied in both the Upper section per scoring instructions and Lower section per scoring instructions, with applicable bonuses being awarded as described. The winner of the game is the player with the highest "Grand Total" score.

## Building Application

Todo

## Generating Doxygen Documentation

To generate the html and latex documentation for this project, cd into the source directory and generate a new Doxyconfig file if it doesn't exist already using:

`doxygen -g`

which will create a default Doxygen config file called `Doxyfile`. Then, you can generate the documentation by doing:

`doxygen Doxyfile`

To help create formatted Doxygen comment blocks in this project, a visual studio plugin was used. Information on the plugin may be found here:

https://marketplace.visualstudio.com/items?itemName=cschlosser.doxdocgen&ssr=false#overview 
