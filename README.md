# NWHL Game Strategy Datathon 

## Objective:
Given stathletes-tracked women’s hockey data from the NWHL, we aim to select five top players to form a competitive team. The players should, ideally, excel in all areas of the game. Since scoring goals is the ultimate objective, at least three should be excellent goal scorers(3 goal most) and at least two should be excellent passers(2 play most).  In addition, we need at least two faceoff (2 face-off win most) specialists and one takeaway specialist (1 takeaway often).  It would be especially beneficial if the passers were familiar with the shooting specialists (given player1 play most, player 2 is among 3 goal most) (i.e., had a good track record of completing passes to these players). 

## Methods:
### 1.Select data on 4 events: Goal, play, face-off win, takeaway
(1)Goal: find each player’s number of successful goal and arrange in descending order. Also calculate successful rate by #goal/(shot+goal) columns
(2)Play: find each player’s number of successful play and arrange in descending order.  Also calculate successful rate by #play/(play+incomplete play) columns
(3)Face-off win: find each player’s number of face-off win and arrange in descending order. 
(4)Takeaway:find each player’s number of takeaway win and arrange in descending order. 

### 2.Establish a ranking system based on each player’s performance.
The idea is to compare all of a player’s valuable events to the frequency in which goals are scored. We took the frequency of each stat to goals. For example, there were 4338 shots on goal between the 2015-16 and 2016-17 seasons, and 461 goals. Take the 461 goals and divide them by the 4338 shots on goal, and you get the factor of .11.

Game_Score= goals + x1play + x2shot + x3faceoff win + x4takeaway - x5penalty taken + X5penalty draw +x6puck_recovery
X1= total goals/ (total play+incomplete play)
X2= total goals/ total (shots+goals)
X3= total gaols / total faceoff win
X4= total goals/ total takeaway
X5= powerplay goals/panalty taken 
X6= total goals/total puck_recovery

Play_Score= plays + x1goal + x2incomplete_play + x3faceoff win + x4takeaway - x5penalty taken + X5penalty draw
X1= play/ (total play+incomplete play)
X2= play/ total (shots+goals)
X3= play / total faceoff win
X4= play/ total takeaway
X5= powerplay play/panalty taken 
X6= play/total puck_recovery

## Analysis
To run the analysis of the datathon:
1. Git clone the entire repository by:
```
git clone https://github.com/Nicole-Tu97/Datathon_Bronze_Winner.gitrl
```
3. Open terminal and set current working directory as the repository.
4. Set up environment for the datathon by copy and enter below code in terminal:
``` 
conda env create --file environment.yml
```
and activate the environment by:
```
conda activate datathon_NWHL
```
5. open jupyter lab by enter:
``` 
jl
``` 
7. open "src/Datathon_analysis.ipynb"
8. click "run all" buttom to run all analysis and steps.  

## Report
The final report can be found
[here](https://github.com/Nicole-Tu97/Datathon_Bronze_Winner/blob/main/report/Datathon-YejunTu_Orange.pdf).

## References
<div id="refs" class="references hanging-indent">

<div id="ref-Ferris2018">
    
Ferris, S. (2018, March 22). An Introduction to NWHL Game Score. Hockey Graphs.

</div>


