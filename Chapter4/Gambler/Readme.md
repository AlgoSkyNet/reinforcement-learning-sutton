## Chapter 4 - Gambler's Problem, Exercise 4.8

### Setup:

A gambler has the opportunity to make bets on the outcomes of a sequence of coin flips. 
If the coin comes up heads, he wins as many dollars as he has staked on that flip; 
if it is tails, he loses his stake. The game ends when the gambler wins by reaching 
his goal of $100, or loses by running out of money. On each flip, the gambler must 
decide what portion of his capital to stake, in integer numbers of dollars. This 
problem can be formulated as an undiscounted, episodic, finite MDP. The state is 
the gambler’s capital, *s* belongs to the set \{1, 2, ..., 99\} and the actions are stakes, 
*a* belonging to the set \{0, 1, .., min(s, 100−s)\}. The reward is zero on all transitions except those on which the 
gambler reaches his goal, when it is +1. The state-value function then gives the 
probability of winning from each state. A policy is a mapping from levels of 
capital to stakes. The optimal policy maximizes the probability of reaching the goal. 
Let p_h denote the probability of the coin coming up heads. If p_h is known, 
then the entire problem is known and it can be solved, for instance, by value iteration. 

Implement value iteration for the gambler’s problem
and solve it for ph = 0.25 and ph = 0.55. In programming, you may find it convenient
to introduce two dummy states corresponding to termination with capital of 0 and
100, giving them values of 0 and 1 respectively. Show your results graphically, as in
Figure 4.3.

### Solution:

I have implemented the solution of the exercise for p_h = 0.25, 0.4 and 0.55 with policy
iteration as well as value iteration algorithms. For p_h = 0.25 we can see that both algorithms 
find the solution resembling the one in the book, while for 0.4, there are much more ties
in the optimal action set. For probability of heads equal to 0.55, the optimal action is 
just betting one unit, as the gambler is sure that in the limit he is going to win, 
so he is maximizing the number of his bets.




