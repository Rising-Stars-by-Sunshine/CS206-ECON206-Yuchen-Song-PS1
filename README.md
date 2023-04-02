# # Title [How to Choice a Good Title?](https://www.nature.com/articles/s41562-021-01152-2)
## Project information
- **Author**: Yuchen Song, Comutation and Design with tracks in Computer Science, Class 2025, Duke Kunshan University
- **Instructor**: Prof. Luyao Zhang, Duke Kunshan University
- **Disclaimer**: Submissions to the Problem Set No. or Final Project for [COMPSCI/ECON 206 Computational Microeconomics, 2023 Spring (Seven Week - Second)](https://ce.pubpub.org/) instructed by Prof. Luyao Zhang at Duke Kunshan University.
- **Acknowledgments**: [How to Acknowledge?](https://www.scribbr.co.uk/thesis-dissertation/acknowledgements/)
[notes: please include all professors, students, and staff who have contributed to your completetion of the project.]
- **Project Summary**: 
  - [Summarize the Background/Motivation]
  - [Research Questions]
  - [Application Scenario]
  - [Methodology]
  - [Results]
  - [Intellectual Merits and Practical impacts of your project.]
  
   
Note: please insert the screenshot of the answers to your research question by ChatGPT. The methodology that you use to address the research questions must be more innovative than both the current literature and ChatGPT. 

## Table of Contents

- model
- code
- spotlight
- more about the author
- references

### Model
- Game Environment

Game Environment the Trust Game is an experiment of choice to study trust in economic interaction. In my customized version of the game, there are two anonymously paired players, A and B, and there are two rounds. The game starts with player A, who is given 1000$ and must decide to send none or some quantity of money to the second player. Money left in player A's account has 2% interest. Then player B receives 3 times the money sent by A and must decide to send none or some quantity of money back to A. Similarly, money left in B's account has 5% interest. Before the second round if A's amount of money is larger or equal to B's amount, then two players will change their roles, which means player A in the first round will be player B in the second round. In the second round, the rule is the same as the one in the first round. 

Possible strategies for the Player who starts with A:
1.	Cooperation: If Player A chooses to trust Player B and give B all the money, then it is possible to maximize the benefit, because according to the rules of the game, Player A gets $500 in both rounds, meaning that both players get $500. But if B doesn't cooperate to maximize benefits, then player A may get less money in the first round or get a little bit more money but lose the opportunity to switch roles in the second round.
2.	Risk aversion: Player A can choose not to give player B any money to get more profit in the first round. This may cause another player also gives nothing in the second round, which is a lose-lose situation.
3.	Reciprocity: The player may choose to give a portion of the money to balance the benefits of both players, which may build trust. And it’s possible that in the second round, another player may continue to play the same strategy, resulting in a similar payoff for both players.

Possible strategies for the Player who starts with B:
1.	Maximizing profits: Player B chooses to give back all the money to Player A in the first round to build trust. In this way, the greatest profit is likely to be made in the second round. 
2.	Control the game: If Player B wants to control the game, in the first round, he can calculate and give Player A small amounts of money back to Player A, so that the roles in the second round cannot be changed.
3.	Risk minimization: In the first round, Player B can choose to keep all his money and pay nothing in the second round as Player A, then he is sure to win.
4.	Reciprocity: In the first round, make both players gain a similar amount of money and successfully switch roles in the second round.

Payoff:

Based on the different strategies of the two players, the payoffs are as follows: 

1.	Win-win situation: If both players trust each other, Player A will receive $500 for both rounds, and both players will gain the maximum money.
2.	Reciprocity but not maximization: If two players build trust by giving money that equalizes the benefits of both, their payoffs will be very similar, which is a number between 102 and 500. However, because they don't give all their money, the total payoff will not be maximized.
3.	None of them choose to cooperate. They will give nothing, and eventually, both will gain $102.
4.	The player that starts with B wants to control the game. In Trust Game, player B has more chance to gain more money than player A. So, one player may want to be player B in both rounds.
5.	One of the players decides not to cooperate or reciprocate. If the player starts with A, then he will keep $100, and gain $102 in the first round. Then in the second round, it will play as B, and it will gain 0 to 106 dollars, based on the money that Player A sends to his. If the player starts with B, then he will gain 1.06 times the money sent by A in the first round and gain $102 in the second round.


- Solution Concept

Based on the backward induction, we can find out solutions for the game. 
In the second round, Player B has the following options to win the game: First, when Player B has more money than player A, Player B can choose to give part or all of his money to Player A so that both players have the same money or almost the same money, which is a reciprocity or maximization benefits situation; B, when B has less money than A, B's total return will be less than A's, whether he pays back A or not; Third, when B has more money than A, B can choose not to give or give less money to A, so that B will have more money than A. 
Cases 1 and 3 (B has more money than A) may be because, in the second round, Player A chose to trust B and gave him most or all of his money. That's the only possible premise. And this player could be either A or B in the first round. If he is A, then he will choose reciprocity or maximization, giving most or all his money to his opponent, who has violated his trust. If he is B, then his opponent, by calculation, may choose to give him less money, making it impossible for him to get more money at the end of the first round. 
For the second case (B has less money than A), it assumes that A gives B less money in the second round or that A's money at the beginning of the second round is greater than 100 plus B's money. In the first case, the strategy for both players in the first round is the same as in the previous paragraph. In the second case, because A gave B almost nothing in the first round, the difference between the two was about 102.


- Evaluations: e.g. efficiency and fairness

### Code
- Game Environment
- Strategic plays
- Equilibruim Evaluations: e.g. belief, strategy, and payoffs
- oTree Experimental Code 


### Spotlight
- Posters
- Figures
- Slides
- Presentations
- Review articles
- Media appearance

### More about the Author
- headshot
- self-introduction
- Final reflections 
  - intellectual growth
  - professional growth
  - living a purposeful life

### References

- Literature References in [Chicago Author-Date](https://www.chicagomanualofstyle.org/tools_citationguide/citation-guide-2.html) Style and [BibTex](https://scholar.google.com/) 

Levin, Dan, and Luyao Zhang. 2020. “Bridging Level-K to Nash Equilibrium.” *The Review of Economics and Statistics* 104 (6): 1329–40. https://doi.org/10.1162/rest_a_00990.

```
@article{levin2022bridging,
  title={Bridging level-k to nash equilibrium},
  author={Levin, Dan and Zhang, Luyao},
  journal={Review of Economics and Statistics},
  volume={104},
  number={6},
  pages={1329--1340},
  year={2022},
  publisher={MIT Press One Rogers Street, Cambridge, MA 02142-1209, USA journals-info~…}
}
```

