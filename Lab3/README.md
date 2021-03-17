# Genetic Algorithms and Epidemic Models
## Part I: Genetic Algorithms
### Description - Steps
Genetic Algorithms are global adaptive heuristic search and optimization techniques modeled from natural selection, genetic and evolution.

The basic steps are:
1. **Start**: Generate random population of m chromosomes (suitable solutions for the problem)
2. **Fitness**: Evaluate the fitness f(x) of each chromosome x in the population
3. **New population**: Create a new population by repeating the following steps until the new population is complete
    1. **Selection**: Select two parent chromosomes from a population according to their fitness (the better fitness, the bigger chance to be selected)
    2. **Crossover**: With a crossover probability cross over the parents to form a new offspring (children). If no crossover was performed, offspring is an exact copy of parents
    3. **Mutation**: With a mutation probability mutate new offspring at each locus (position in chromosome)
    4. **Accepting**: Place new offspring in a new population
    5. **Replace**: Use new generated population for a further run of algorithm
4. **Test**: If the end condition is satisfied, stop, and return the best solution in
current population
5. **Loop**: Go to step 2

### Application 1: OneMax Problem
We develop a genetic algorithm to solve the OneMax Problem, which is a simple problem consisting in maximizing the number of ones of a bitstring. We optimize the solution by 
testing different values of parameters such as crossover probability, mutation probability, elitism, size of population, etc. We achieve score 18 in a bitstring of 20 bits.

### Application 2: Community Detection
![Capture](https://user-images.githubusercontent.com/50949470/111471753-e6c8d200-8731-11eb-81a8-6cbeb03fe9eb.PNG)
* **Representation**: Each individual is a vector of size N (number of nodes), where the value j at position i means a link between nodes (i,j). 
Such links should exist in the original network. We find communities represented by each individual via finding connected components. 
Similar to OneMax Problem, we optimize the solution by testing different values of parameters.
* **Results**: We compare the genetic algorithm results with those of community detection algorithms studied in [Lab2](https://github.com/chrisbetze/Social-Network-Analysis/blob/5a88a73f8e5ba5eec3ab8b40902f1cf6f0833e14/Lab2/Lab2.ipynb).

## Part II: Epidemic Models
<img src="https://user-images.githubusercontent.com/50949470/111477670-07942600-8738-11eb-8e8d-59b756580f48.png" width="700" height="500">

We try to find numerical solutions of the basic epidemiological SIR and SIS models. Some useful parameters are:
* The contact rate of actors: β
* Τhe mean recovery (healing) rate: γ
* Basic reproduction number: R0

### SIR Model
We apply some different values of parameters and we study the behaviour of the model in relation to R0.

### SIS Model
For the SIS model, we adopte the case of periodic node contact rate. This may correspond to a recurrence of epidemics, such as the usual influenza virus. 
We apply some different values of parameters and we study the behaviour and the evolution of the model.
