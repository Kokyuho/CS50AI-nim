# CS50’s Introduction to Artificial Intelligence with Python
# Project 4: Learning: Nim

**Aim**: Write an AI that teaches itself to play Nim through reinforcement learning.

**Description**: In the game Nim, we begin with some number of piles, each with some number of objects. Players take turns: on a player’s turn, the player removes any non-negative number of objects from any one non-empty pile. Whoever removes the last object loses.

There’s some simple strategy you might imagine for this game: if there’s only one pile and three objects left in it, and it’s your turn, your best bet is to remove two of those objects, leaving your opponent with the third and final object to remove. But if there are more piles, the strategy gets considerably more complicated! 

In this problem, we build an AI that can learn the strategy for this game through reinforcement learning. By playing against itself repeatedly and learning from experience, our AI will learn which actions to take and which actions to avoid.

In particular, we’ll use Q-learning for this project. In Q-learning, we try to learn a reward value (a number) for every (state, action) pair. An action that loses the game will have a reward of -1, an action that results in the other player losing the game will have a reward of 1, and an action that results in the game continuing has an immediate reward of 0, but will also have some future reward.

See more info about our model here: https://cs50.harvard.edu/ai/2020/notes/4/#q-learning

Full problem set description here: https://cs50.harvard.edu/ai/2020/projects/4/nim/

Usage:
```
python play.py
```

Example:
```
$ python play.py
Playing training game 1
Playing training game 2
Playing training game 3
...
Playing training game 9999
Playing training game 10000
Done training

Piles:
Pile 0: 1
Pile 1: 3
Pile 2: 5
Pile 3: 7

AI's Turn
AI chose to take 1 from pile 2.
```
