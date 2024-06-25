We are asked to work with the Markov Chain Monte Carlo algorithm, in
particular the Metropolis-Hastings algorithm. The aim is to simulate random numbers
for the distribution with probability density function given below
f(x) = 1/2 exp (−|x|)
(a) Apply the random walk Metropolis algorithm using N = 10000 and s = 1. Use the
generated samples (x1, . . . xN ) to construct a histogram and a kernel density plot in
the same figure. Note that these provide estimates of f(x).Overlay a graph of f(x) on
this figure to visualise the quality of these estimates. Also, report the sample mean
and standard deviation of the generated samples (Note: these are also known as the
Monte Carlo estimates of the mean and standard deviation respectively).
Practical tip: To avoid numerical errors, it is better to use the equivalent criterion
log u < log r (x∗, xi−1) = log f (x∗) − log f (xi−1) instead of u < r (x∗, xi−1).
(b) The operations in part 1(a) are based on the assumption that the algorithm has
converged. One of the most widely used convergence diagnostics is the so-called Rb
value. In order to obtain a valued of this diagnostic, you need to apply the
procedure below:
• Generate more than one sequence of x0, . . . , xN , potentially using different
initial values x0. Denote each of these sequences, also known as chains, by
(x(j)0, x(j)1, . . . , x(j) N) for j = 1, 2, . . . , J
