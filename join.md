#### join


1. Modify it to show the matchid and player name for all goals scored by Germany. To identify German players, check for: teamid = 'GER'
* SELECT matchid, player FROM goal WHERE teamid = 'GER'

2. Show id, stadium, team1, team2 for just game 1012
* (close but rows repeat) SELECT id, stadium, team1, team2 FROM game INNER JOIN goal ON matchid WHERE id = 1012

