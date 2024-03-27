# How to Estimate the number of shots to use on H-series Devices?

### Step 1: Number of Two Qubit Gates
Find the number of two qubit gates in the circuit, since two qubit gate error is the dominant error in the quantum simulations. Let it be $N$

$$ N = \text{Number of Two Qubit Quantum Gates}$$

### Step 2: Circuit Fidelity
Calculate Circuit Fidelity~ the probability of our quantum circuit succeeding.

$$ c \approx f^{N}$$

where $c:$ circuit fidelity, $f:$ two-qubit gate fidelity and $N=$ Number of two qubit gates.

### Step 3: Estimate Shot Number

#### Confidence Interval Approximation 

$$ \hat{p} \pm z \sigma $$

$$ \sigma = \frac{\hat{p}(1- \hat{p})}{n}$$

where $\hat{p}$ is the binomially-ditributed observation, $\sigma$ is the standard deviation , and $n$ is the number of experiments.

and $z:  1- \frac{\alpha}{2}$ quantile. At $95%$ , $z \approx 2$.

Now framing this in context of quantum circuit, we have

#### Approximate Distribution of Error

$$ c \pm 2 \sigma $$

$$ \sigma = \frac{c(1- c)}{s}$$

wjere $c$ is the circuit fidelity, circuit successful or not, $\sigma$ is the standard deviation of circuit error, and $s$ is the number of shots.


#### Goal 
Differentiate between noise and set of bitstrings you're after with high degree of confidence

$$ c - 2\sigma >0 \rightarrow c-2 \sqrt{\frac{c(1-c)}{s}} > 0 \rightarrow s > \frac{4(1-c)}{c}$$

but there are some caveates regarding this formula, that we need to account for:
1. The estimate is unreliable for small sample sizes.
2. Doesn't work for success probabilities close to $0$ or $1$.

To count for these, we must consider
1. Ensuring $s$ becomes large enough.
2. Circuit Fidelity, $c$ should not be near $0$ or $1$

To do this we introduce a constant factor $k$

$$ s > k \frac{4(1-c)}{c}$$


But what should $k$ be?

The central limit theorem suggests, as the number of shots increases, binomial distribution approximates the Gaussain normal distribution.

Let's see an example, for two devices, with fidelity $99.6%$ and $99.8%$ respectively, with $N=100$ two qubit gates, and $k=100$, we need

$$ \text{Machine 1 }: s > 100 \frac{1(1-.996^{100})}{.996^{100}} = 197 $$

$$ \text{Machine 2 }: s > 100 \frac{1(1-.998^{100})}{.998^{100}} = 89 $$


We can scale it up to $N=1000$ two qubit gates.

$$ \text{Machine 1 }: s > 100 \frac{1(1-.996^{1000})}{.996^{1000}} = 21,615 $$

$$ \text{Machine 2 }: s > 100 \frac{1(1-.998^{1000})}{.998^{1000}} = 2,562 $$