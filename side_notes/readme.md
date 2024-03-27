# How to Estimate the number of shots to use on H-series Devices?

### Step 1: Number of Two Qubit Gates
Find the number of two qubit gates in the circuit, since two qubit gate error is the dominant error in the quantum simulations. Let it be $N$

$$ N = \text{Number of Two Qubit Quantum Gates}$$

### Step 2: Circuit Fidelity
Calculate Circuit Fidelity~ the probability of our quantum circuit succeeding.

$$ c \approx f^{N}$$

where $c:$ circuit fidelity, $f:$ two-qubit gate fidelity and $N=$ Number of two qubit gates.

### Step 3: Estimate Shot Number

Confidence Interval Approximation 

$$ \hat{p} \pm z \sigma $$

$$ \sigma = \frac{\hat{p}(1- \hat{p})}{n}$$

where $\hat{p}$ is the binomially-ditributed observation, $\sigma$ is the standard deviation , and $n$ is the number of experiments.

and $ z:  1- \frac{\alpha}{2}$ quantile. At $95\%$ , $ z \approx 2$