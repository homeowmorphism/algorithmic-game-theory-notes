## Some remarks 

* Come to office hours! They empty he lonely. Friday 3-4 pm. 
* **Braess' paradox** - take some time to go through it, it takes a few hours to get it. 
* Slides have been updates - time to redownload them.

# Zero-Sum Games

Constant reward is constant in all outcomes. Leads to "zero-sum thinking". We are going to focus on two-player zero-sum games. 

Ex: rock paper scissors -- zero sum game because the sum of all outcomes is zero. 
Non-ex: prisoners dilemma. Both players can prefer the same outcome - this never happens in zero sum games. 

Why are they interesting?
* Most games we play are zero sum (chess, rock-papz, tic-tac-toe).
* (win, lose), (lose, win), (draw, draw)

Why are they technically interesting? 
* Relation between rewards of player 1 and player 2
* Reward for P2 = - Reward P1

## Rewards in Matrix form
*What about mixed strategies?*

Let $$x_1 = (x_{1,1}, x_{1,2}, \dots)$$, the reward is $$x_1^T * A * x_2$$

## Maximin Strategy

* I want to max my strategy. P2 is going to try to min, so I will max over the min. 

{% math %}
V_1^* = \max_{x_1} \min_{x_2} x_1^T * A * x_2
{% endmath %}

I.e. I can at least guarantee myself $$V_1^*$$.

P2 is going to do the same. -- As a result, $$V_1^* = V_2^*$$ since both players will strategize $$V_1^* \geq V_2^*$$, $$V_1^* \leq V_2^*$$. 

**Theorem** for any 2p-zs game, the reward of both player is the same. Set of Nash equilibria $$\{(x_1^*, x_2^I): x_1^* \text{maximin}, x_2^* \text{minimax}$$ i.e. $$x_1^*, x_2^*$$ are the best strategies respectively.

## Proof of Minimax Theorem
See slide.

Here we used stronger thm to prove weaker one.

*Can compute this optimal strategy quickly?* Yes! Using linear programming!

$$x_1 \dots x_n$$, maximize

{% math %}
\max_{x_1, \dots, x_n} \sum_{i=1}^{n} f_i x_i
{% endmath %}

subject to: 

{% math %}
a_{1,1} x_1 + \dots + a_{1,n} x_n \leq b_1 A x \leq b
a_{2,1} x_2 + \dots + a_{2,n} x_n \leq b_2 A x \leq b
\dots
{% endmath %}

Solving this system is *linear programming*. In particular here we are going to guarantee $$\geq v$$ for the outcome.

## Minimax theorem in real life

* Players don't always play the minimax strategy, or follow Nash equilibrium.
* Need to update based on player strategy -- lots of active literature on how to optimize when this happens.

Ex: soccer example. (see slides p.24), this is real data -- suggests that in high stakes situation people play their minimax strategy.


## More on Minimax Theorem

It doesn't really have to do with game theory, all you need is a mathematical statement. Given a lin. sys. as described, the order of min/max'ing doesn't matter! This is used say to prove *Yao's principle* which provides lower bounds for randomized algorithm. **This is equivalent to linear programming duality!**

-- Pause to worship some dudes blabla von Neumann legend kk we know oh wait kk he suggests some YouTube videos too as another form of worship media k great bai! --
