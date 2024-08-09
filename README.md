# Adaptive Particle Swarm Optimization (APSO) Study on CEC2017 Benchmark Suite

<div align="center">
    <img src="https://miro.medium.com/v2/resize:fit:786/format:webp/0*ufjlAeNxGSWpPj8S" alt="Particle Iteration" width="400px"/>
</div>


## Overview

This repository presents a comprehensive comparative analysis of Standard Particle Swarm Optimization (PSO) and a novel Adaptive PSO (APSO) algorithm across the CEC2017 benchmark suite. Our study investigates the performance of both algorithms on 30 diverse test functions, spanning unimodal, multimodal, hybrid, and composition problems, across dimensions of 10, 30, 50, and 100.

## Key Features

- Implementation of Standard PSO and novel APSO algorithms
- Comprehensive testing on CEC2017 benchmark functions
- Performance analysis across 10, 30, 50, and 100 dimensions
- Convergence analysis and visualization
- Novel application to bin packing problem

## Algorithms

### Standard PSO vs Adaptive PSO (APSO)

<div align="center">
    <table>
        <tr>
            <td align="center">
                <img src="https://github.com/svdexe/PSO-vs-APSO-CEC2017-/blob/main/Peudo%20Codes/Standard%20PSO%20SVD.png" alt="Standard PSO Pseudocode" width="400px"/>
                <p>Standard PSO Pseudocode</p>
            </td>
            <td align="center">
                <img src="https://github.com/svdexe/PSO-vs-APSO-CEC2017-/blob/main/Peudo%20Codes/Adaptive%20PSO%20SVD.png" alt="Adaptive PSO Pseudocode" width="400px"/>
                <p>Adaptive PSO Pseudocode</p>
            </td>
        </tr>
    </table>
</div>

### Description

**Standard PSO** forms the baseline for our comparison, utilizing fixed parameters throughout the optimization process.

**Adaptive PSO (APSO)** incorporates:
- Dynamic adjustment of inertia weight and acceleration coefficients.
- Stagnation detection and reset mechanism.
- Enhanced ability to escape local optima.


## CEC2017 Benchmark Functions

| **Typology**                      | **No.** | **Function name**                                      | **Optimum** |
|-----------------------------------|---------|--------------------------------------------------------|-------------|
| **Unimodal Functions**            |         |                                                        |             |
|                                   | 1       | Shifted and Rotated Bent Cigar                         | 100         |
|                                   | 2       | Shifted and Rotated Sum of Different Power             | 200         |
|                                   | 3       | Shifted and Rotated Zakharov                           | 300         |
| **Simple Multimodal Functions**   |         |                                                        |             |
|                                   | 4       | Shifted and Rotated Rosenbrock                         | 400         |
|                                   | 5       | Shifted and Rotated Rastrigin                          | 500         |
|                                   | 6       | Shifted and Rotated Expanded Schaffer F6               | 600         |
|                                   | 7       | Shifted and Rotated Lunacek Bi-Rastrigin               | 700         |
|                                   | 8       | Shifted and Rotated Non-Continuous Rastrigin           | 800         |
|                                   | 9       | Shifted and Rotated Levy                               | 900         |
|                                   | 10      | Shifted and Rotated Schwefel                           | 1000        |
| **Hybrid Functions**              |         |                                                        |             |
|                                   | 11      | Hybrid Function 1 (N=3)                                | 1100        |
|                                   | 12      | Hybrid Function 2 (N=3)                                | 1200        |
|                                   | 13      | Hybrid Function 3 (N=3)                                | 1300        |
|                                   | 14      | Hybrid Function 4 (N=4)                                | 1400        |
|                                   | 15      | Hybrid Function 5 (N=4)                                | 1500        |
|                                   | 16      | Hybrid Function 6 (N=4)                                | 1600        |
|                                   | 17      | Hybrid Function 7 (N=5)                                | 1700        |
|                                   | 18      | Hybrid Function 8 (N=5)                                | 1800        |
|                                   | 19      | Hybrid Function 9 (N=5)                                | 1900        |
|                                   | 20      | Hybrid Function 10 (N=6)                               | 2000        |
| **Composition Functions**         |         |                                                        |             |
|                                   | 21      | Composition Function 1 (N=3)                           | 2100        |
|                                   | 22      | Composition Function 2 (N=3)                           | 2200        |
|                                   | 23      | Composition Function 3 (N=3)                           | 2300        |
|                                   | 24      | Composition Function 4 (N=4)                           | 2400        |
|                                   | 25      | Composition Function 5 (N=5)                           | 2500        |
|                                   | 26      | Composition Function 6 (N=5)                           | 2600        |
|                                   | 27      | Composition Function 7 (N=6)                           | 2700        |
|                                   | 28      | Composition Function 8 (N=6)                           | 2800        |
|                                   | 29      | Composition Function 9 (N=3)                           | 2900        |
|                                   | 30      | Composition Function 10 (N=3)                          | 3000        |


## Features

- Native implementation of all CEC 2017 single objective functions optimized for multiple simultaneous evaluations.
- Pre-defined rotations, shifts, and shuffles for 2, 10, 20, 30, 50, and 100 dimensions.
- Allows custom rotations, shifts, and shuffles.
- Convenient surface plot utility.
- Easy access to basic functions f1 to f19 (e.g., Ackley, Discus, etc.).

As per the problem definitions, functions are defined for 10, 30, 50, and 100 dimensions, with functions f1 to f10 and f21 to f28 also being defined for 2 and 20 dimensions. If you provide custom rotation matrices (and shuffles, where applicable), you can, however, use arbitrary dimensions. Below are some surface plots for functions f1 to f10 over 2 dimensions.

## Visual Representation

![CEC2017 Functions Surface Plot](https://raw.githubusercontent.com/tilleyd/cec2017-py/master/extra/plots.jpg)

[1] Awad, N. H., Ali, M. Z., Suganthan, P. N., Liang, J. J., & Qu, B. Y. (2016). Problem Definitions and Evaluation Criteria for the CEC 2017 Special Session and Competition on Single Objective Bound Constrained Real-Parameter Numerical Optimization.



## Results Highlight

Our comprehensive analysis reveals:

- APSO consistently outperforms standard PSO in solution quality and convergence speed
- The performance gap widens with increasing problem complexity and dimensionality
- APSO exhibits enhanced ability to escape local optima and maintain swarm diversity
- APSO shows improved scalability in higher dimensions, maintaining good performance where standard PSO struggles

## Real-World Application: Bin Packing

We propose a novel two-stage application of APSO to the bin packing problem:

1. **Clustering Stage**: Using APSO for object clustering instead of conventional methods like KNN
2. **Packing Stage**: Employing APSO to optimize the packing of clustered objects

This approach leverages APSO's demonstrated strengths in both continuous (clustering) and discrete (packing) optimization spaces, potentially offering more flexible and efficient solutions to complex, multi-stage optimization challenges.


