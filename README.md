# Datathon
# Objective:
GIven stathletes-tracked women’s hockey data from the NWHL, we aim to select five top players. The players should, ideally, excel in all areas of the game. Since scoring goals is the ultimate objective, at least three should be excellent goal scorers(3 goal most) and at least two should be excellent passers(2 play most).  In addition, you need at least two faceoff (2 face-off win most) specialists and one takeaway specialist (1 takeaway often).  It would be especially beneficial if the passers were familiar with the shooting specialists (given player1 play most, player 2 is among 3 goal most) (i.e., had a good track record of completing passes to these players). 
# Methods:
# 1.Select data on 4 events: Goal, play, face-off win, takeaway
(1)Goal: find each player’s number of successful goal and arrange in descending order. Also calculate successful rate by #goal/(shot+goal) columns
(2)Play: find each player’s number of successful play and arrange in descending order.  Also calculate successful rate by #play/(play+incomplete play) columns
(3)Face-off win: find each player’s number of face-off win and arrange in descending order. 
(4)Takeaway:find each player’s number of takeaway win and arrange in descending order. 
# 2.Establish a ranking system based on each player’s performance.
https://hockey-graphs.com/2018/03/22/an-introduction-to-nwhl-game-score/
The idea is to compare all of a player’s valuable events to the frequency in which goals are scored. Dom’s Game Score includes goals, assists, shots on goal, penalties drawn and taken, faceoffs won and lost, blocked shots, 5v5 goal differential, and 5v5 Corsi differential.
Took the frequency of each stat to goals. For example, there were 4338 shots on goal between the 2015-16 and 2016-17 seasons, and 461 goals. Take the 461 goals and divide them by the 4338 shots on goal, and you get the factor of .11.
Skater Game Score = Goals + (.64*Assist) + (.11*Shot on goals) + (.12*Faceoff win) – (.12*Face off lose) – (.17*Penalty taken) *took the frequency of powerplay goals to penalties.
an assist is when up to two players of the scoring team shoots, passes or sends the puck towards the scoring teammate, or touched it in any other way which made the goal. 
https://hockey-graphs.com/2019/08/21/revisiting-nwhl-game-score/#more-23764
To build upon Shawn’s initial NWHL game score formula, I added primary and secondary assists and two more years of data to his work. I adjusted the value of primary and secondary assists against the frequency of goals. Adding two more seasons of data changed the initial weights that Shawn had for shots on goal, faceoffs, and penalties taken.
Skater Game Score = G + (.90*primary assists) + (.66*secondary assists) + (.10*Shot on goals) + (.11*Faceoff win) – (.11*Face off lose) – (.15*penalties taken)+ (.15*PEND)

# Below are scores for our dataset based on above info:
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
