# NBA 2018-19 Analysis

Analysis of various facets and storylines of the 2018-2019 NBA regular season using numpy, pandas, matplotlib and seaborn.

All data is courtesy of [Basketball Reference](https://www.basketball-reference.com/) unless otherwise noted.

## CONTENTS:
- NBA Trends Analysis
- MVP RACE 2019
- Bestbrook or Worstbrook?
- The Veteran Effect
- Consitency is key (coming soon)
- Player "Portability" (coming soon)
- Most Improved Player(s) (Figures in Repo)

## NBA Trends Analysis

### Introduction:

I wanted to look into to two phenomena of the modern NBA: Tanking and the Three Point/Small Ball revolution.

### #TheProcess

In the NBA, tanking is when a franchise loses games on purpose to get a better (higher) draft choice. This is most famously personified today by the Philidelphia 76ers who went through "The Process" and were terrible on a historical level for a number of years in a row. I wanted to see if this strategy was:

A) Actually effective

and

B) the expected timeline/range of results of this strategy

For this figure I took all the teams from 2000-2012 who had a first overall pick and mapped average changes in Win Percentage over a five-year post-pick period.

![alt text](https://github.com/wilsonmacleod/NBA-2018-19_Analysis/blob/master/NBA_Trends/figs/theprocess.png)

Based on my analysis franchises generally "peak" in terms of win percentage in the 3rd and 4th years after a obtaining and using a first overall pick. With the highest variance of results coming the 5th season. This timeline aligns perfectly with the initial four-year rookie contract, with the variance in the fifth year being explained by a team’s ability to keep and/or build around their newfound star. Outside of a few outliers this strategy has proven to be very effective with the averages of all seasons post number one pick showing a 15%+ increase in Win Percentage.

## The Three Point Revolution

### Introduction:

I wanted to see if I could track the impact the success of the Golden State Warriors and their style of play have had on the league.

### Three Point Revolution
 
 First, I wanted to see if the much-publicized increase in 3-point shooting league-wide was as signifigant as it has been made out to be. Second, if that increase in 3-point attempts led to more points per game and if there was a positive correlation between 3s attempted and Wins and Losses and finally if that correlation was more/less signifigant at different time intervals in the last 10 NBA seasons.
 
![alt text](https://github.com/wilsonmacleod/NBA-2018-19_Analysis/blob/master/NBA_Trends/figs/3PAvPTS.png)

There has been a strong correlation between 3s attempted and points per game since 2012.

![alt text](https://github.com/wilsonmacleod/NBA-2018-19_Analysis/blob/master/NBA_Trends/figs/3PAvRk.png)

Although there is a correlation between 3s attempted and finishing position in the league, it hasnt necessarily been impacted signifigantly by the massive uptick of 3s attempted per game.

### "Small Ball"

I wanted to see if the play-style swing that accompanied the 3-point revolution, "small ball", could be quantified and if there was a signifigant change in the way guards and forwards have begun playing. Small ball is generally playing with only 1 or 0 traditional "big men or playing with a 4 position who can spread the floor and shoot open long-distance shots.

I examined players from the 2009-2019 seasons and classified their positions based on Basketball References listed positions as well as consolidating hybrid roles (PG-SG = PG, SF-PF = SF etc.) I also only included players who played more than 30 games and averaged 10 or more minutes per game.

![alt text](https://github.com/wilsonmacleod/NBA-2018-19_Analysis/blob/master/NBA_Trends/figs/3PA_pos-boxen.png)

Since the Warriors exploded on to the scene and won the 2015 championship the rate at which "big men", especially 4s, attempt 3s has exploded. 

![alt text](https://github.com/wilsonmacleod/NBA-2018-19_Analysis/blob/master/NBA_Trends/figs/3PA_pos-line.png)

In 2018 players classified as playing the 4 or "PF" actually attempted on average more 3s than players playing in the traditional wing forward or "small forward position.

## MVP RACE 2019
 
### Introduction:

As the 2018-2019 NBA regular season winds down (2 days left) the MVP race is looking like a two-horse race. **James Harden** and **Giannis Antetkounmpo** are pretty far out ahead of the pack and the general consensus is that one or the other will end up winning the NBA's most prestigious individual award. I wanted to see if I could find any blatant statistical, both "normal" and advanced, advantages for either side. And, while the end winner of the award usually comes to narrative or media/fan favoritism, see if I could determine statistically who should win based purely on the measurables.

### Harden's Insane Usage Rate:

The first thing that stood out to me in this race is the amount each player is being asked to do by their team. Usage rating is determined by the amount of possessions "used" by a player during their time on the floor, this means anytime the teams possession ends with the player:
- Attempting a field goal 
- Shooting Free-throws 
- Turning the ball over. 

The Rockets lean heavily on Harden each and every game, over 40% of their plays while he is on the floor end with a Harden action. He is also 2nd in the league in Minutes Played emphasizing the game by game demand the Rockets place on him.

![alt text](https://github.com/wilsonmacleod/NBA-2018-19-Analysis/blob/master/MVP_Race/figs/TotalMinsUsage.png)

(Players with <500 minutes played (~10 full games) were not included in the figure as there are some meaningless high usage ratings in there (read garbage time chuckers.))

Given Harden's unheard-of usage rate and his heavy minutes load, his scoring efficiency and shooting must be suffering right? Wrong. True Shooting Percentage (TS%) is a stat that factors and weighs 2-point shots, 3 point shots and free throws and aims to gauge a players true efficiency at scoring the ball. Harden is currently leading the league in points per game by a sizable margin while maintaining a shooting efficiency that is above the leagues other leading scorers. Giannis is no slouch in this department either being tied for the lead in TS% for players above 20 points per game while not shooting threes.

![alt text](https://github.com/wilsonmacleod/NBA-2018-19-Analysis/blob/master/MVP_Race/figs/ScoringTS.png)

This sustained performance despite hefty load is also evident in the two's PER scores. PER is Player Efficiency Rating, PER strives to measure a player's per-minute performance, while adjusting for pace.

![alt text](https://github.com/wilsonmacleod/NBA-2018-19-Analysis/blob/master/MVP_Race/figs/PERvUSG.png)
### The Ying and The Yang

So what are the keys to these two superstars offensive games? Getting to the line! Both Dominant the game scoring wise in their own ways, Giannis in the paint (2 pointers) and Harden from Three (only Steph Curry has him beat in makes per game.) But the thing they both have in common is they attempt and make free throws at a very high clip.

![alt text](https://github.com/wilsonmacleod/NBA-2018-19-Analysis/blob/master/MVP_Race/figs/ScoringRoots.png)

Harden leads the league in free throws attempted and made per game, but is this a product of flopping? Skill? Favoritism from the refs? Free throw rate is the number of free throw attempts per field goal attempt. While Harden is getting to the line with more volume than the rest of the league this may be down to his crazy usage rating and the volume of shots he is taking. Giannis and Joel Embiid are actually getting to the line at a higher rate per field goal attempt.

![alt text](https://github.com/wilsonmacleod/NBA-2018-19-Analysis/blob/master/MVP_Race/figs/FreeThrowRate.png)

### The "Other" Side of The Ball

Defensive impact is very hard to quantify even using advanced stats and lets be honest the MVP award is rarely decided on the defensive side of the ball. Giannis dominates the defensive boards and blocks a good amount of shots while Harden gets steals at a suprising rate.

![alt text](https://github.com/wilsonmacleod/NBA-2018-19-Analysis/blob/master/MVP_Race/figs/generalDEF.png)

## Bestbrook or Worstbook?

### Introduction

Russell Westbrooks pros and cons as basketball player are well documentated throughout the NBA-sphere. I wanted to see if I could find any interesting trends in his play this season.

### Triple Double Machine

In 2018-19 Westbrook had one of his worst shooting seasons in his career, but the other parts of his stat-sheet stuffing game did not falter. By the end of the season, on average, it was more likely for him to end a game with a triple double than it was for him to make a given field goal. He ended the season shooting 42% from the field, with 46% of his 73 games played being recorded as triple doubles.

![alt text](https://github.com/wilsonmacleod/NBA-2018-19_Analysis/blob/master/Russ/figs/tripledoubles_fg.png)

### Smart plays and Dumb plays

Westbrook finds and creates opportunities for his teammates at a league leading rate, his major downfall this season has been his love of shooting threes. 

![alt text](https://github.com/wilsonmacleod/NBA-2018-19_Analysis/blob/master/Russ/figs/russ_subplot.png)

His three-point habit also effects how the team performs... The more threes he attempts the 'lower' the Thunder's point differential. Unsuprisingly his assist tally increasing has the opposite effect. 

![alt text](https://github.com/wilsonmacleod/NBA-2018-19_Analysis/blob/master/Russ/figs/3pa_pointdiff.png) ![alt text](https://github.com/wilsonmacleod/NBA-2018-19_Analysis/blob/master/Russ/figs/ast_pointdiff.png)

More coming soon on Russ...

## The Veteran Effect

### Introduction:

In today's NBA, players are expected to hit the ground running at a very young age. I wanted to see if I could find any effects of experience/age in terms of productivity on either side of the ball. For these figures I used all players aged 18-37 from the years 2000-2019.

### Young Athleticism vs. Veteran Savvy?

As player age increases offensive rating increases while defensive rating starts declines, particulary rapidly at about 30 years old. This analysis matches up with the conventional wisdom that most players "peak" at around ages 26-30 and it takes a while for young players to adjust offensively. 

![alt text](https://github.com/wilsonmacleod/NBA-2018-19_Analysis/blob/master/Vets/figs/ratings.png)

### Experience Is the Greatest Teacher

Players also make "smarter plays" as they age they commit fouls and turnover the ball at a lower rate as they get older and gain more League experience. 

![alt text](https://github.com/wilsonmacleod/NBA-2018-19_Analysis/blob/master/Vets/figs/to_pf.png)

On average they also shoot at a lower rate and make passes leading to teammates scoring at a higher rate as they age.

![alt text](https://github.com/wilsonmacleod/NBA-2018-19_Analysis/blob/master/Vets/figs/pts_ast.png)
