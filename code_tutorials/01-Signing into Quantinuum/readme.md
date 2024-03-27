## How to submit H-series Devices?

### Workflow

1. Syntax Checker (Eg H1-1SC) : Ensure that your quantum circuit will run on Quantinuum hardware before submitting jobs. Checks the quantum circuit syntax against a device's compiler. Free to use, does not require H-system quantum credits.

2. Emulator (Eg. H1-1E) : Classical emulation of the H-series quantum computers. Realistic physical and noise models of the devices. Includes the devices unique software features. Requires HQCs.

3. Hardware (Eg. H1-1) : Trapped Ion Quantum Computers, Requires HQC


```python
pip install pytket, pytket-quantinuum
```



