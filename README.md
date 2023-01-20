# mlb_data
SQL project for the 2022 MLB season showcasing custom queries to reveal batting and pitching statistics! 

This 2022 statisticle data was pulled from :
https://www.kaggle.com/datasets/vivovinco/2022-mlb-player-stats

The mlb_stats database contains 2 tables as follows

The Pitching Table:

DESC pitching;

+-------+--------+------+-----+---------+-------+
| Field | Type   | Null | Key | Default | Extra | Field Description
+-------+--------+------+-----+---------+-------+
| Rk    | int    | YES  |     | NULL    |       | Rk : Rank
| Name  | text   | YES  |     | NULL    |       | Name : Player name
| Age   | int    | YES  |     | NULL    |       | Age : Player age
| Tm    | text   | YES  |     | NULL    |       | Tm : Team
| Lg    | text   | YES  |     | NULL    |       | Lg : Leauge 
| W     | int    | YES  |     | NULL    |       | w : Wins
| L     | int    | YES  |     | NULL    |       | L : Losses
| W-L%  | double | YES  |     | NULL    |       | W-L% : Win-Loss percentage
| ERA   | double | YES  |     | NULL    |       | ERA : 9 * ER / IP 
| G     | int    | YES  |     | NULL    |       | G : Games played
| GS    | int    | YES  |     | NULL    |       | GS : Games Startred
| GF    | int    | YES  |     | NULL    |       | GF : Games Finsihed 
| CG    | int    | YES  |     | NULL    |       | CG : Complete Games
| SHO   | int    | YES  |     | NULL    |       | SHO : Shutouts
| SV    | int    | YES  |     | NULL    |       | SV : Saves
| IP    | double | YES  |     | NULL    |       | IP : Innings Pitched
| H     | int    | YES  |     | NULL    |       | H : Hits allowed
| R     | int    | YES  |     | NULL    |       | R : Runs allowed 
| ER    | int    | YES  |     | NULL    |       | ER : Earned runs allowed
| HR    | int    | YES  |     | NULL    |       | HR : Home runs allowed
| BB    | int    | YES  |     | NULL    |       | BB : Bases on balls/walks
| IBB   | int    | YES  |     | NULL    |       | IBB : Intentional bases on balls
| SO    | int    | YES  |     | NULL    |       | SO : Strikeouts
| HBP   | int    | YES  |     | NULL    |       | HBP : Times hit by a pitch
| BK    | int    | YES  |     | NULL    |       | BK : Balks
| WP    | int    | YES  |     | NULL    |       | WP : Wild pitches
| BF    | int    | YES  |     | NULL    |       | BF : Batters faced
| ERA+  | int    | YES  |     | NULL    |       | ERA+ : 100 * (logERA/ERA)
| FIP   | double | YES  |     | NULL    |       | FIP : Fielding independent pitching. Measures a pitcher's effectiveness at HR, BB, HBP and causing SO.
| WHIP  | double | YES  |     | NULL    |       | WHIP : (BB + H) / IP
| H9    | double | YES  |     | NULL    |       | H9 : 9 * H / IP
| HR9   | double | YES  |     | NULL    |       | HR9 : 9 * HR / IP
| BB9   | double | YES  |     | NULL    |       | BB9 : 9 * BB / IP
| SO9   | double | YES  |     | NULL    |       | SO9 : 9 * SO / IP
| SO/W  | double | YES  |     | NULL    |       | SO/W : SO / W
+-------+--------+------+-----+---------+-------+


The Batting Table: 

DESC batting;

+-------+--------+------+-----+---------+-------+
| Field | Type   | Null | Key | Default | Extra | Field Description
+-------+--------+------+-----+---------+-------+
| Rk    | int    | YES  |     | NULL    |       | Rk : Rank
| Name  | text   | YES  |     | NULL    |       | Name : Player Name
| Age   | int    | YES  |     | NULL    |       | Age : Player Age
| Tm    | text   | YES  |     | NULL    |       | Tm : Team
| Lg    | text   | YES  |     | NULL    |       | Lg : League
| G     | int    | YES  |     | NULL    |       | G : Games Played 
| PA    | int    | YES  |     | NULL    |       | PA : Plate Appearances 
| AB    | int    | YES  |     | NULL    |       | AB : At Bats 
| R     | int    | YES  |     | NULL    |       | R : Runs Scored 
| H     | int    | YES  |     | NULL    |       | H : Hits 
| 2B    | int    | YES  |     | NULL    |       | 2B : Doubles Hit
| 3B    | int    | YES  |     | NULL    |       | 3B : Triples Hit
| HR    | int    | YES  |     | NULL    |       | HR : Home Runs Hit
| RBI   | int    | YES  |     | NULL    |       | RBI : Runs Batted In
| SB    | int    | YES  |     | NULL    |       | SB : Stolen Bases
| CS    | int    | YES  |     | NULL    |       | CS : Times Caught Stealing
| BB    | int    | YES  |     | NULL    |       | BB : Bases On Balls / Walked 
| SO    | int    | YES  |     | NULL    |       | SO : Strike outs
| BA    | double | YES  |     | NULL    |       | BA : Hits/at bats (Batting Average) 
| OBP   | double | YES  |     | NULL    |       | OBP : (H + BB + HBP) / (AB + BB + HBP + SF)
| SLG   | double | YES  |     | NULL    |       | SLG : Total bases/at bats or (1B + 2 * 2B + 3 * 3B + 4 * HR) / AB
| OPS   | double | YES  |     | NULL    |       | OPS : On-base + Slugging percentages
| OPS+  | int    | YES  |     | NULL    |       | OPS+ : 100 * (OBP / logOBP + SLG / logSLG - 1)
| TB    | int    | YES  |     | NULL    |       | TB : Total bases
| GDP   | int    | YES  |     | NULL    |       | GDP : Double plays grounded into
| HBP   | int    | YES  |     | NULL    |       | HBP : Times hit by a pitch
| SH    | int    | YES  |     | NULL    |       | SH : Sacrifice hits
| SF    | int    | YES  |     | NULL    |       | SF : Sacrifice flies
| IBB   | int    | YES  |     | NULL    |       | IBB : Intentional bases on balls
+-------+--------+------+-----+---------+-------+
