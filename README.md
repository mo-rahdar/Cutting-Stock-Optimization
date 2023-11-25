# Cutting-Stock-Optimization
The cutting-stock problem is a challenge encountered in manufacturing and production optimization. This problem involves the efficient cutting of standard-sized pieces of stock material, such as paper rolls or sheet metal, into smaller pieces of specified sizes. The primary objective is to minimize material waste during the cutting process.

# Cutting Stock Optimization

The key characteristic of the cutting-stock problem lies in its inherent complexity and the potential for generating a vast number of different product units from a single master roll. The challenge is not only to determine how to cut the stock material to meet specific size requirements but also to find the optimal combination of cuts that minimize wasted material. Given the multitude of potential combinations, the task is non-trivial, requiring sophisticated optimization techniques to identify the most efficient and economical cutting patterns. This problem is particularly relevant in industries where maximizing material utilization and minimizing waste are critical factors for cost-effectiveness and sustainability.


## Table of Contents

- [Introduction](#introduction)
- [Usage](#usage)
- [Requirements](#requirements)
- [Installation](#installation)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## Introduction

In operations research, the cutting-stock problem is the problem of cutting standard-sized pieces of stock material, such as paper rolls or sheet metal, into pieces of specified sizes while minimizing material waste. This project provides a solution to the cutting-stock problem using optimization techniques.

## Usage

To use the cutting stock optimization code:

1. Install the required dependencies.
2. Run the code with your specific input data.
3. Analyze the output patterns and scrap values.

## Requirements

- Python 3
- Pyomo (Python Optimization Modeling Objects)
- glpk solver

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/cutting-stock-optimization.git
    cd cutting-stock-optimization
    ```

2. Install the required dependencies:

    ```bash
    pip install pyomo
    ```

## Examples

Here's a simple example of how to use the cutting stock optimization code:

```python
# Provide your input data and run the optimization

# A list of specified sizes
orders = [10.75, 11, 13, 14.5, 15, 19.5, 21, 22.5, 23, 24, 25, 26, 27.5, 28, 30, 32, 34, 36, 48, 68.5]
# The minimum required amount for each specified size
demand = [2, 2, 7, 8, 4, 2, 12, 4, 4, 10, 18, 2, 17, 2, 7, 4, 4, 6, 3, 2]
# The standard sizes of the stock materials
stock = [120, 144]
# The maximum possible number of pieces in each pattern
k = 5

# Run the function to create possible patterns
dfp, dfa, dfc, dfd = pattern(orders, demand, stock, k)

# Create the optimization model and solve it

# Print the optimized patterns and results
```
