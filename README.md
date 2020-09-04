# Reinforcement Learning

Reinforcement Learning is one of the most exciting fields of Machine Learning, producing many applications, particularly in **games**(TD-Gammon, a Backgammon-playing program) and **machine control**. In 2013, researchers from a British startup called DeepMind demonstrated a system that could learn to play just about any Atari game from scratch, eventually outperforming humans in most of them, **using only raw pixels as inputs and without any prior knowledge of the rules of the games**. They applied the power of deep learning to reinforcement learning.

## Learning to optimize rewards

In Reinforcement Learning, a software **agent** makes **observations** and takes **actions** within an **environment**, and in return it receives **rewards**. Its objective is to learn to act in a way that will **maximize its expected rewards over time**. In short, the **agent acts in the environment and learns by trial and error to ***maximize its pleasure*** and ***minimize its pain.***

## Examples

Controlling a robot, Atari game, Alpha Go, thermostat, stock market prices, self-driving cars, recommender systems, placing ads on a web page, or controlling where an image classification system should focus its attention.

## Policy

The algorithm a software **agent** uses to determine its **actions** is called its **policy**. The policy could be a neural network taking observations as inputs and outputting the
action to take.

###### Policy Search

This **learning algorithm** is to try out many different values for various parameters(like probability and angle), and pick the combination
that performs best. **Brute force approach**. When the policy space is too large (which is generally the case), finding a good set of parameters this way is like searching for a needle in a gigantic haystack.

###### Genetic Algorithm

Another way to explore the policy space is to use **genetic algorithms**. For example, you could randomly create a first generation of 100 policies and try them out, then “kill” the 80 worst policies and make the 20 survivors produce 4 offspring each. An offspring is a copy of its parent plus some random variation. The surviving policies plus their offspring together constitute the second generation. You can continue to iterate through generations this way until you find a good policy.

***If there is a single parent, this is called asexual reproduction. With two (or more) parents, it is called sexual reproduction. An offspring’s genome (in this case a set of policy parameters) is randomly composed of parts of its parents’ genomes.***

***One interesting example of a genetic algorithm used for Reinforcement Learning is the NeuroEvolution of Augmenting Topologies (NEAT) algorithm.***

###### Policy Gradients(PG)

Another approach is to use **optimization techniques**, by evaluating the gradients of the rewards with regard to the policy parameters, then tweaking these parameters by following the gradients toward higher rewards..

***This is called Gradient Ascent. It’s just like Gradient Descent but in the opposite direction: maximizing instead of minimizing.***
