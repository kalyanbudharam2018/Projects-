## Approach:
The Cricket Tournament Simulation Program is designed to simulate a cricket match involving two teams. The program uses classes to represent different entities like players, teams, field, umpire, and commentator. Each class has specific attributes and methods to mimic real-world cricket matches and statistics. The simulation is controlled by the Match class, which handles the match's progress, including innings, overs, scores, and wickets.

## Methodology:

### Class Definitions:

* Player: Represents individual players with attributes such as name, batting, bowling, fielding, running, and experience.
* Teams: Represents the two cricket teams with a name and a list of players. It has methods for adding players and selecting a captain.
* Field: Represents the cricket field with attributes like field size, fan ratio, pitch conditions, and home advantage.
* Umpire: Handles the prediction of outcomes for each ball based on random probabilities. It keeps track of scores, wickets, and overs.
* Commentator: Provides commentary for each ball and over based on the match statistics.

* Match Class:

The Match class is responsible for controlling the overall simulation of the cricket match.
It tracks the progress of the match, including innings, overs, scores, and wickets.
The match is played in two innings, and each inning has a specified number of overs.
After the first innings is completed, the innings is changed, and the second innings begins.
The match ends after the second innings, and the final result is displayed based on the scores of both teams.

* Simulation Logic:

The match simulation is performed by the simulate_match method in the Match class.
The method simulates each ball and over of both innings using the Umpire and Commentator classes.
The outcome of each ball, such as runs scored and wickets, is determined based on the players' probabilities.
The scores and wickets are updated accordingly, and commentary is provided for each ball and over.

* Output:

The program provides output throughout the simulation, including commentary for each ball and over.
The final output displays the final scores of both teams, the number of wickets lost, and the match result (Team 1 wins, Team 2 wins, or a tie).


* Methodology Used:

- The program follows an object-oriented approach, with each entity represented as a class with its attributes and methods.
- The simulation logic uses random number generation to predict ball outcomes based on player probabilities.
- The match is simulated using a loop to play each ball and over, and the innings are switched when required.
- The match results are calculated based on the scores and wickets of both teams at the end of the match.



Overall, the Cricket Tournament Simulation Program provides a basic and simplified simulation of a cricket match with two teams. It showcases how different classes can interact to create a realistic simulation of real-world scenarios. Depending on the complexity and depth required, additional features and details can be added to enhance the simulation further.




