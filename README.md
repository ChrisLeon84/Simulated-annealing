# Simulated-annealing
The following was the final assignment for a graduate course in computational physics.  

The task was to find the global minimum of a function via [simulated annealing](https://en.wikipedia.org/wiki/Simulated_annealing). The difficulty was that the function had many local minima. The entire code was written from scratch. 

The simulation starts with N =1000 particles in a 2 dimensional box, uniformly distributed in space and normally distributed in momentum (this was based on the expected distribution for an ideal gas, so should be approximately correct at high "temperatures"). Also there was a "temperature" of 100.   Equilibrium is then achieved via Markov chain Monte Carlo (specifcally, the [Metropolis-Hastings algorithm](https://en.wikipedia.org/wiki/Metropolis%E2%80%93Hastings_algorithm)). The temperature is subsequently lowered and the process repeated. If done correctly the particles should inhabit the global minimum at sufficiently low temperatures. The rate of cooling had to be found by running the code over and over. The issue: too quick and the particles don't all settle in the global minimum, too slow and the code takes way too long to run. Also, the number of trials for Metropolis Hastings to run after each temperature drop was found empirically.

TL;DR:
1. Give random intial conditions for particles
2. Get to an equilibirum state for tempterature T (start at 100)
3. Lower temperature
4. Go to 2. while lowered T >0 .
5. Particles should inhabit the global minimum when done. 

Playing around, the correct rate of cooling was found. The global minima is known and the algorithm did indeed correctly identify it (eventually).
