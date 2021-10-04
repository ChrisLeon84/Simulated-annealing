# Simulated-annealing
The following was the final assignment for a course in computational physics.  

The task was task was the to find the global minimum of a function via [simulated annealing](https://en.wikipedia.org/wiki/Simulated_annealing). The difficulty was that the function had many local minina The entire code was written from scratch. 

The simulation starts with N =1000 particles in a 2 dimensional box, uniformly distributed in space and normally distributed in momentum. Also there was a "temperature" of 100.   Equilibrium is then achieved via Markov chain Monte Carlo (specifcally, the [Metropolis-Hastings algorithm](https://en.wikipedia.org/wiki/Metropolis%E2%80%93Hastings_algorithm)). The temeperature is subsequently lowered and the process repeated. If done correctly the particles should inhabit the global minimum at sufficiently low temperatures. The rate of cooling had to be found by running the code over and over. To quick and the particles don't all settle in the global minimum. Too slow and the code takes way too long to run.
