# Mahoraga Strategy Algorithm for Iterated Prisoner's Dilemma

## Overview
The **Mahoraga** strategy is a dynamic algorithm for the **Iterated Prisoner's Dilemma** (IPD). It adapts to the opponent's behavior using various techniques, including **Tit for Tat** detection, **Random detection**, **Grudge mode**, and **Cooperation rate checks**. The strategy aims to cooperate initially but will defect in response to exploitation by the opponent.

## Key Features
- **Tit for Tat Detection**: Detects if the opponent follows a **Tit for Tat** strategy (mirroring the player's previous moves). If detected, the player will cooperate.
- **Random Strategy Detection**: Identifies if the opponent uses a **random strategy** based on the proportion of cooperations. If detected, the player will defect.
- **Grudge Mode**: If the opponent defects 6 times in a row while the player cooperated at least twice, **Grudge mode** is triggered, causing the player to permanently defect.
- **Cooperation Rate Check**: Monitors the player's cooperation rate (over 80%) in the last 3 moves. If the opponent defects after this cooperation, the player will defect after detecting this pattern 4 times to avoid exploitation.
- **Pavlov Strategy**: Follows the **Win-Stay, Lose-Shift** principle—if the last round’s moves match (both cooperated or both defected), the player repeats the previous move. Otherwise, the player switches their choice.

## Algorithm Logic
 
1. **Tit for Tat Detection**: 
    - If the opponent mirrors the player’s previous moves, the player will cooperate.

2. **Random Strategy Detection**: 
    - If the opponent’s moves appear random, the player will defect.

3. **Grudge Mode**: 
    - If the opponent defects 6 times consecutively, and the player cooperated at least twice during that period, the strategy switches to permanent defection (Grudge mode).

4. **Cooperation Rate Check**: 
    - The algorithm tracks cooperation rate over the last 3 moves. If the cooperation rate is over 80% and the opponent defects afterward, the strategy will defect if this pattern is detected 4 times to avoid being exploited.

5. **Pavlov Strategy**: 
    - If both the player and opponent cooperated or defected in the previous round, the player repeats the previous action. If there was a mismatch (cooperate vs defect), the player switches to defect.

## Conclusion
The **Mahoraga** strategy combines adaptive mechanisms such as **Tit for Tat**, **Grudge mode**, and **Pavlov** to effectively handle the Iterated Prisoner's Dilemma. It aims to cooperate when possible but will switch to defection if the opponent exploits cooperation, ensuring a balanced approach to the game.