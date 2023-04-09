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


- Evaluations: 

  Efficiency:
  The game seems to be designed in a way that encourages players to send money to each other and build trust. The 2% and 5% interest rates provide an incentive for players to keep their money in their account, but the potential gains from receiving money from the other player may encourage them to take a risk and send some money to the other player. This can lead to a positive outcome where both players benefit from the exchange and build trust over time.

  Fairness:
  At first glance, the game may seem unfair since player A is the only one who has the initial decision to send money or not, while player B has more chance to gain more money than player A. However, in the customized version, this is mitigated by the fact that in the second round, the roles are reversed, and player B has the opportunity to send money to player A. However, there's still a limitation that player B can send back a small amount of moneny to prevent role reversal in round two. If that happens, the game is still unfair and player B in round one has more chances to win the game. Additionally, the fact that players are anonymous and paired randomly ensures that there is no inherent bias or discrimination based on factors such as race, gender, or socioeconomic status.

  Overall, the Trust Game seems to be an efficient and fair game that can provide valuable insights into how trust is built in economic interactions.

### Code
- Description on how you customize the demo.
  
  Endowment: In my customized trust game, the endowment is $1000. I think the increase in the amount of money can induce participants not to return the money.
  
  Interest rate: In the new trust game, interest rates are added to induce participants to keep the money. Meanwhile, adding more variables can complicate the situation and increase the amount of thought for participants to make rational thinking harder.
 
  Role exchange: In the customized version, the game has two rounds. When the first-round finishes, players have the chance to exchange their roles. Since in the demo, player A is the weak party, for passively receiving multiplied money, the new rule is set, which is exchanging roles when Player A’s money is less or equal to Player B’s money after the first round. However, the new rule cannot fully eliminate the unfairness of the game. Since Player B can send a little bit more money back to exchange his role and gives nothing to the other player in the second round to gain more payoffs. 

- Explain how you think subjects’ behavior playing the customized demo might be different 
from the behavior playing the oTree demo and why.

### Spotlight
- Behavioral experimental research
 
  The paper on behavioral experimental research is “Trust, Reciprocity, and Social History” by James Berg, John Dickhaut, and Kevin McCabe.
  
  In the paper, the authors design several experiments of trust games, where they have to decide how much to give each other and how much to keep for themselves. By   conducting these behavioral experiments, the researchers found that participants have some extent of trust in anonymous counterparts, which verifies that reciprocity is a fundamental element of human behavior. Their second finding is that social history is important in human behavior. In the experiments, participants who have positive previous interactions with others are more likely to trust and reciprocate and those with negative ones are less likely to do so (Berg, Dickhaut, and McCabe 1995).

  Research question: The author intends to study trust and reciprocity in an investment environment and address the question of how social history (past interaction with others) influences trust and reciprocity in human economic behavior. 

  How does behavior in the experiments differ from backward induction?

  Backward induction assumes that participants can always make rational decisions under different circumstances during experiments or games. However, in the experiments, participants do not always choose the optimal choice. Specifically, in this paper, researchers find that social history and past interaction are factors influencing participants’ decisions (Berg, Dickhaut, and McCabe 1995). Overall, behavioral experiments that are designed to emphasize and study some human behavioral characteristics, may be more likely to induce participants’ irrational decisions and the differences between backward induction and real situation are significant.

  What is the behavioral (e.g., psychological, social) foundation that underpins the observed behavior?

  The first behavioral foundation is reciprocity, which refers to responding to others’ positive actions with another kind and positive action. In the behavioral experiment, the researchers found that participants tend to reciprocate others even though their decision may lead to not reaching the maximum payoff (Berg, Dickhaut, and McCabe 1995). Another behavioral foundation is that social history and past interactions have impacts on decision-making, even if the past and present situations are different.


- Reinforcement learning paper

  In the paper, "A Deep Reinforcement Learning Framework for the Financial Portfolio Management Problem" the authors present a reinforcement learning model to seek a solution to the problem of the portfolio management problem, which is the process of redistributing a fund into different financial products (Jiang, Xu, and Liang 2017). They emphasize the importance of this problem in finance and point out the limitations and disadvantages of some traditional portfolio management methods that cannot show the complexity of markets.

  What is the game environment and the learning algorithm?

  The game environment is built by trading experiments done in the exchange Poloniex, which is a Digital currency trading platform, where there are about 80 tradable cryptocurrencies. Among them, the authors select 11 top-volumed cryptocurrencies and use the historic trading data of these currencies to train the agent (Jiang, Xu, and Liang 2017). 

  In this paper, the reinforcement learning solution framework uses a deterministic policy gradient algorithm, which is a model-free reinforcement learning algorithm used to train an agent to learn optimal and continuous control policies (Silver et al. 2014). Its advantage is that it focuses on deterministic policies, which can be more efficient and makes fewer errors. 

  How are the strategies from the reinforcement learning agents inspires you on trust building among humans?

  One important concept in reinforcement learning is exploration and exploitation. During training, the agents must find a balance between exploiting or simulating behaviors that result in high rewards by analyzing precious data and exploring new strategies that may lead to higher rewards. Similarly, in human interaction, building trust is also a process of exploration and exploitation. For instance, using the previous method of interaction can lead to a similar payoff as previous times. However, to enhance the trust or keep the relationship, new methods must be explored to reach better payoffs. Meanwhile, another important concept is setting incentives, which encourage the agent to reach the research goal. In trust building among humans, we can also use a similar reward-setting method. Overall, the methodologies and strategies in training reinforcement learning agents can provide insights into trust building of human interactions.

### More about the Author
- headshot
- self-introduction
- Final reflections 
  - intellectual growth
  - professional growth
  - living a purposeful life

### References

- Literature References in [Chicago Author-Date](https://www.chicagomanualofstyle.org/tools_citationguide/citation-guide-2.html) Style and [BibTex](https://scholar.google.com/) 

Berg, Joyce, John Dickhaut, and Kevin McCabe. 1995. “Trust, Reciprocity, and Social History.” Games and Economic Behavior 10 (1): 122–42. https://doi.org/10.1006/game.1995.1027.

Jiang, Zhengyao, Dixing Xu, and Jinjun Liang. 2017. “A Deep Reinforcement Learning Framework for the Financial Portfolio Management Problem.” ArXiv.org. 2017. https://arxiv.org/abs/1706.10059.

Silver, David, Guy Lever, Nicolas Heess, Thomas Degris, Daan Wierstra, and Martin Riedmiller. 2014. “Deterministic Policy Gradient Algorithms.” Proceedings.mlr.press. PMLR. January 27, 2014. http://proceedings.mlr.press/v32/silver14.html.

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

