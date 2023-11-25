# Cutting-Stock-Optimization
The cutting-stock problem is a challenge encountered in manufacturing and production optimization. This problem involves the efficient cutting of standard-sized pieces of stock material, such as paper rolls or sheet metal, into smaller pieces of specified sizes. The primary objective is to minimize material waste during the cutting process.

# The Problem

<img src="carpenter_cutting_wood_wit.png" align="right" width="300px"/>
The key characteristic of the cutting-stock problem lies in its inherent complexity and the potential for generating a vast number of different product units from a single master roll. The challenge is not only to determine how to cut the stock material to meet specific size requirements but also to find the optimal combination of cuts that minimize wasted material. Given the multitude of potential combinations, the task is non-trivial, requiring sophisticated optimization techniques to identify the most efficient and economical cutting patterns. This problem is particularly relevant in industries where maximizing material utilization and minimizing waste are critical factors for cost-effectiveness and sustainability. This project provides a solution to the cutting-stock problem using optimization techniques. You need to provide the specified orders to cut from the stock material, the demand for each piece, and the standard size of the stock materials.
<br clear="left"/>

## Table of Contents

- [Usage](#usage)
- [Requirements](#requirements)
- [Examples](#examples)

## Usage

To use the cutting stock optimization code:

1. Install the required dependencies.
2. Run the code with your specific input data.
3. Analyze the output patterns and scrap values.

## Requirements

- Python 3
- Pyomo (Python Optimization Modeling Objects)
- glpk solver

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
