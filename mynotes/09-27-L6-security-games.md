## So far

We've played with *non-binding* contracts. 

# Sequential Move Games

* Focus on two players: "leader" and "follower". 
* Leader first commits to playing a (possibly mixed) strategy $$x_1$$, and cannot backtrack.
* The leader communicates $$x_1$$ to the follower -- follower must believe leader's commitment is credible. 
* Follower chooses the best response $$x_2$$. Can assume this to be a pure strategy. By principle of indifference, if two strats have the same reward there will be a randomization in between the two -- which one matters. 

This is a new framework because in a simultaneous game, the move is non-binding (whereas here we've already played our action). 

*Youtube video of golden balls - split or steal?* [here](https://www.youtube.com/watch?v=S0qjK3TWZE8)

	| Split | Steal
Split | (6.5 K, 6.5 K) | (13 K, 0)
Steal | (13 K, 0) | (0, 0)

The guy managed to turn Prisoner's into a sequential game by convincing the person he's going to steal. 

## How to represent the game?

We can represent the game as a tree. 

## Curious case (see slide p.9)
Nash equilibrium is (1,1) for simultaneous game, but if non-simultanous, would be (2,1) because P2 can commit to play Down. 

It can be even more advantageous in expectation because can commit to up-down (0.49, 0.51), so Exp(P2) is still better if commit to play right. 

**The optimal reward for the leader in the Stackelberg game (commit first) is always greater or equal to the maximum reward under any Nash equilibrium of the simultaneous move version.**

Intuitively: locks opponent into less options to min your reward over in the Minimax formula (p.15)

And surprisingly, this is easier to solve computationally (can be done in polynomial time - which you can't do with Nash equilibrium).

## Applications: Security Games

Defender (leader) wants to defend a set of $$n$$ target $$T$$. Attacker plays after defender.

The time is polynomial in the number of strategies pf the defender, but the number of strategies is exponential is $$k$$, the number of patrol units.on right. 

Randomization is used for a list of real-world security, like protecting entry points to LAX or fare evasion in LA metro (which had to be fixed because bathroom breaks -- omg why didn't they include this in the first place?)
