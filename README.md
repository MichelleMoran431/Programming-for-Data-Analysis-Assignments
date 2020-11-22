#### Assignment : The NumPy.Random Package in Python


Overview of the Jupyter notebook , reference : Data Analysis Programming Assignment 

NB: The following Examples of code include importing  : 

import numpy as np
from numpy.random import default_rng


---

 ##### Introduction - Overall use of the NumPy.random
 
 Examples of using Random Generator: 
 
 Code#1  outputs a list of 4 random numbers less than 10 
 
 Code#2  Using the bit generator PCG64 and passing it through the generator to call a random number
 
 Code#3  Using the legacy bit generator MT19937 and passing it through the Generator to call a random number
 
 ---

 
 ##### The use of the "Simple random data" and " Permutations" functions
 
 ###### Simple random data 
 
 Table given to show the examples of simple random data and their parameters
 
 Code#4  Example of Integers :Using default_rng and setting the dtype for integers to ouput an array of 10 integers between 0 and 10
 
 Code#5  Example of Choice : generating 3 random samples from a given 1-D array
 
 ##### Permutations
 
 Defined Permutions and its 2 options : 
 
 Code#6  Using the permutation function to create a random password. Starting with an array of the alphabet called Letters and asking it to output 6 random letters and leaving the original array unchanged
 
 Code#7  Using the shuffle function to give random lotto numbers. Firstly create an list of the numbers 1- 43 to create an array from. Then draw out the first 6 random numbers. 
 
 ---
 
 ##### The use and purpose of at least five " Distributions" Functions
 
 For each of the 5 distributions given for following information was discussed along with code and graph examples : 
 
 Distributions :Normal , Binomial, Poisson , Pareto , Rayleigh 
 
 Information : Definition , Syntax used, Parameters defined, real examples and other distribution comparisons, Examples given with graphic displays.
 
 
 *1. Normal Distribution : 
 
 Code#8 Using the parameters mu,sigma as 0,0.1. and the default_rng.normal syntax. Output random values of 1000.
 Then using the probabilty density function in a histogram (import matplotlib.pyplot as plt), visualising the results , a classic bell shaped curve is observed showing the majority of the results are in and around the mean value. 
 

*2. Binomial Distribution : 

Looked at the difference between the normal and binomial distributions , did a comparison using a distplot using the same size no.

Code#9  The example of flipping the a coin 10 times. Using the parameters (n)no. of trials, (p) probability of occurence = 10, SIze =0.5   and the default_rng.binomial syntax. Output random values of 10. The result is the number of heads per experiment ( 10) of 10 flips of the coin. 


Code#10 Another example of using binomial distribution to randomly work out the flipping of the coin but using the Scipy.stats module to calculate the binomial distribution and matplotlib to visualise the results. 

*3. Pareto Distributon :

Code#11 using the syntax: np.random.default_rng().pareto(a, 1000) + 1) * m. Also visualising the the classic pareto J shaped curve. 

*4. Poisson Distribution: 

Code#12 using the syntax: rng.poisson(1am =, size=) to determine the probability number of occurances over a specified time. The other example given is the measurement of radioactive decay. 

*5.Rayleigh Distribution : 

Code#13 using the syntax rng.rayleigh(modevalue, 1000000) (mode =, size=). Wave heights area are an example of data that follow a rayleigh distribution. 

Here you need to calculate the meanvalue in order to calculate the mode value. using np.sqrt(2 / np.pi) * meanvalue. Input the answer into the syntax.

---

#### The Use of Seeds in Generating Pseudorandom Number 

 
The terms PRNG pseudorandom number generator was defined and explained by looking at Generators and bitGenerators. 
Two types of bit generators were examined , MT19937 which is deemed a legacy now and the new bitgenerator called the PCG64. 
 
A comparsion table was given between the two bitgenerators. One significant difference was the performance timings. PCG64 being the fastest. 
 
Another signicant difference is the seeding these algorithms. Either seeding or determining the seed. Using random.seed() function in the legacy bitgenerator MT19937 , one can determine the random number. see example code 1 , shows creating a seed from random.randrange( sys.maxsize) and then inputing into the rand.seed function. 

NB: Please take note of the seed value and random number , this had to be done by yourself, the computer doesnt automatically save this. 

This seed value can then be inputed into example 2 , random.seed () , in order to reproduce the random number from example 1. 

This process is easy using the MT19937 , however for the PCG64, the process of determining a seed is more difficult involving entropy values etc. However one can allocate a seed number see example 3. Here the result will always be the same , once the seed is the same. 
