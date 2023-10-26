# Getting Started with pytket

[![License](https://img.shields.io/github/license/quantinuum/pytket)](https://github.com/quantinuum/pytket/blob/main/LICENSE)

Welcome to the pytket repository! Pytket is a versatile quantum computing toolkit developed by Quantinuum, designed to make it easier for you to work with quantum circuits, quantum compilation, and more.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Documentation](#documentation)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Quantum computing is an exciting and rapidly evolving field, and pytket aims to simplify the development of quantum software. Whether you're a beginner or an experienced quantum programmer, pytket can be a valuable tool in your quantum computing journey.

## Installation

To get started with pytket, you'll need to install it. You can install it via pip:

```bash
pip install pytket
```

For more installation options and details, please refer to the [Installation Guide](https://github.com/quantinuum/pytket#installation).

## Usage

Once you have pytket installed, you can start using it in your projects. Here's a simple example of creating a quantum circuit:

```python
from pytket import Circuit

# Create a quantum circuit
circuit = Circuit(2)

# Add gates to the circuit
circuit.H(0)
circuit.CX(0, 1)

print(circuit)

```

For more examples and details on how to use pytket, visit the [Getting Started Guide](https://github.com/quantinuum/pytket#getting-started).


## Documentation

You can find detailed documentation and examples in the [official pytket documentation](https://pytket.readthedocs.io/).



## Contributing

Contributions are welcome! If you'd like to contribute to the development of pytket or report issues, please refer to our [Contribution Guidelines](https://github.com/quantinuum/pytket/blob/main/CONTRIBUTING.md).


## License

Pytket is open-source and available under the [MIT License](https://github.com/quantinuum/pytket/blob/main/LICENSE).
