# Homework 03

### Exercise 1

1. Draw the Bayesian Network representing the joint distribution

$$P(A,B,C,D,E,F,G)=P(A)P(B|A)P(F|B)P(C|A)P(D|B)P(E|D,F)P(G).$$

2. Indicate whether the following statements on (conditional) independence are True or False and motivate your answer.

 a. $A\perp \!\!\! \perp  D$
 
 b. $F \perp \!\!\! \perp  D$
 
 c. $A\perp \!\!\! \perp  B | C$
 
 d. $A\perp \!\!\! \perp  D | B$
 
 e. $D\perp \!\!\! \perp  F | E$

 f. $B\perp \!\!\! \perp F| E$
 
 g. $A\perp \!\!\! \perp  D | \{B, F\}$

### Exercise 2

1. Write the generative model represented by the following directed graph, knowing that:
    - $p$ and $\pi_j$ are sampled from Beta distributions;
    - $r_i$ is sampled from a Bernoulli distribution;
    - $u_{ij}$ is sampled from a Bernoulli distribution with parameter $r_i (1 - \pi_j) + (1 - r_i)\pi_j$.
  

!

1. Implement the generative model using `pyro`. 

    Set the hyperparameters to $\alpha_p=1,\beta_p=1,\alpha_\pi=1,\beta_\pi=5$ and evaluate your model on the observations `data = dist.Bernoulli(0.6).sample((12,6))`.

    Remember to use plate notation and to condition on the observed data!
