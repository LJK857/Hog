# Hog
根据cs61a框架独立完成的hog项目，用来记录Python的学习

如果你想玩这个游戏，那么用集成终端打开hog文件夹并输入

python3 hog_gui.py

则可以打开gui界面，那么就可以玩耍了

下面是游戏的规则
Rules
In Hog, two players alternate turns trying to be the first to end a turn with at least GOAL total points, where GOAL defaults to 100. On each turn, the current player chooses some number of dice to roll, up to 10. That player's score for the turn is the sum of the dice outcomes. However, a player who rolls too many dice risks:

Sow Sad. If any of the dice outcomes is a 1, the current player's score for the turn is 1.

Example 1: The current player rolls 7 dice, 5 of which are 1's. They score 1 point for the turn.

Example 2: The current player rolls 4 dice, all of which are 3's. Since Sow Sad did not occur, they score 12 points for the turn.

In a normal game of Hog, those are all the rules. To spice up the game, we'll include some special rules:

Boar Brawl. A player who rolls zero dice scores three times the absolute difference between the tens digit of the opponent’s score and the ones digit of the current player’s score, or 1, whichever is higher. The ones digit refers to the rightmost digit and the tens digit refers to the second-rightmost digit. If a player's score is a single digit (less than 10), the tens digit of that player's score is 0.

Example 1:

The current player has 21 points and the opponent has 46 points, and the current player chooses to roll zero dice.
The tens digit of the opponent's score is 4 and the ones digit of the current player's score is 1.
Therefore, the player gains 3 * abs(4 - 1) = 9 points.
Example 2:

The current player has 45 points and the opponent has 52 points, and the current player chooses to roll zero dice.
The tens digit of the opponent's score is 5 and the ones digit of the current player's score is 5.
Since 3 * abs(5 - 5) = 0, the player gains 1 point.
Example 3:

The current player has 2 points and the opponent has 5 points, and the current player chooses to roll zero dice.
The tens digit of the opponent's score is 0 and the ones digit of the current player's score is 2.
Therefore, the player gains 3 * abs(0 - 2) = 6 points.
Sus Fuss. We call a number sus if it has exactly 3 or 4 factors, including 1 and the number itself. If, after rolling, the current player's score is a sus number, they gain enough points such that their score instantly increases to the next prime number.

Example 1:

A player has 14 points and rolls 2 dice that total 7 points. Their new score would be 21, which has 4 factors: 1, 3, 7, and 21. Because 21 is sus, the score of the player is increased to 23, the next prime number.
Example 2:

A player has 63 points and rolls 5 dice that total 1 point. Their new score would be 64, which has 7 factors: 1, 2, 4, 8, 16, 32, and 64. Since 64 is not sus, the score of the player is unchanged.
Example 3:

A player has 49 points and rolls 5 dice that total 18 points. Their new score would be 67, which is prime and has 2 factors: 1 and 67. Since 67 is not sus, the score of the player is unchanged.
