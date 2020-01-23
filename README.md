# PID-Controller-Tuning-using-Genetic-Algorithm

### Abstract
PID controller is widely used in industries. Its application varies from a small industry to big scale industries. Working with this controller is in the daily routine of the people who works in big industries. Now, the main problem arises with the optimization of PID controller. There are various ways of optimization e.g. Ziegler Nicholas which is a basic method and Advanced method such as Genetic Algorithm.

The idea is to tune the parameters of the PID controller, as a result of a improved genetic algorithm which combines the concept of multi objective optimization. Genetic Algorithm(GA) is a stochastic global search method that imitates the process of natural evolution. The GA is basically based on an iterative process of selection, recombination, mutation, and evaluation. It is based on Darwin's theory of natural evolution and the concept of 'survival of the fittest'. Genetic Algorithms are capable of locating high-performance areas in complex domains without experiencing many difficulties associated with high dimensionality or false optima which might occur with the gradient descent techniques. 

The simulations are done using MATLAB. First, the classical methods like Ziegler Nicholas is used to tune the parameters and then MultiObjective function with fixed weights and also with optimum weights was used. Using the GA method, the same model is redesigned with MultiObjective function. Collective comparison and analysis of the results of all designs are done, and conclusions are drawn out of the simulation work. The adequacy of proposed algorithm is likewise checked for a framework with an unstable plant and furthermore with Ball and Hoop framework.

### Genetic Algorithm
![alt text](https://github.com/kpilkk/PID-Controller-Tuning-using-Genetic-Algorithm/blob/master/genetic_algorithm.jpg "Logo Title Text 1")

### Multi-Objective Function
The most important step in implementing GA is to determine the objective functions which are used to assess the fitness of each individual. For minimizing the error, we have taken the help of linprog function, which calculates the value of weights corresponding to minimum function value unlike previous time, where these were randomly taken. We also took non-linear multi-obejective function to see if it can improve the result. As we want to minimize the error. So fitness function is taken as the inverse of the error. For the implementation of modified genetic algorithm to tune the PID controller rise time, settling time and peak overshoot is used as performance criterion. 

LMO = w1*MP + w2*ts + w3*tR   MO = w1*MP2 + w2*ts1.8 + w3*tR  

The solution can be broadly viewed in the four following sub problems:
  * Decreasing the percentage overshoot(%Mp).  
  * Improving rise time(tr).  
  * Improving Settling time(ts).  
  * Using the multiobjective function for optimization of fitness function.  
