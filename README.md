# Mobile-Games-A-B-Testing-with-Cookie-Cats 🍪🐈
Hello! This's a study case taken from DataCamp. Cookie Cat is a popular mobile puzzle game developed by Tactile Entertainment. So game contains various levels with increasing difficulty.
This project implements an analysis of an A/B test where the first gate in the **Cookie Cats** was moved from level 30 to level 40.
This study seeks to quantify the effect of the change on player retention.

## Problem Statment
In mobile game development, player retention is a key metric for long-term success. 
The game Cookie Cats includes a progression feature called a gate, which temporarily blocks access to the next level.
An A/B test was conducted in the mobile game **Cookie Cats** to evaluate the impact of changing the gate level on player retention. Players were split into two groups:

  **• Group A**: Gate at level 30

  **• Group B**: Gate at level 40

The goal of investigation is to determine whether moving the gate from level 30 to level 40 has a statistically significant effect on 1-day and 7-day retention.

## Data Description
The data we have is from 90,189 players that installed the game while the AB-test was running.
|    Name        |    Type   | Description |
| :---           |    :---:  |   :---     |
| userid         | _int_     | Unique identifier for each player. |
| version        | _string_  | Whether the player was put in the control group (gate_30 - a gate at level 30) or the group with the moved gate (gate_40 - a gate at level 40). |
| sum_gamerounds | _int_     | Total number of game rounds played by the player during the first 14 days after installed.   |
| retention_1    | _boolean_ | If the player returned to the game 1 day after installation set True, else False.     |
| retention_7    | _boolean_ | If the player returned to the game 7 days after installation set True, else False.    |

## Results
***1-Day Retention***

A slight decrease in 1-day retention was observed when the gate was moved from level 30 (44.8%) to level 40 (44.2%).
Bootstrapping was applied to estimate the sampling distribution and assess variability in retention rates.
The results indicate a marginally higher expected retention rate when the gate is positioned at level 30.

***7-Day Retention***

Similarly, 7-day retention decreased from 19.0% (gate at level 30) to 18.2% (gate at level 40).
Bootstrapped sampling distributions suggest a high likelihood (approaching 100%) that retention is greater when the gate remains at level 30.
