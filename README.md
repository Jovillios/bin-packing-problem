# VM Bin Packing Optimizer

![Python](https://img.shields.io/badge/python-3.12-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Dependencies](https://img.shields.io/badge/dependencies-numpy%20|%20scipy-orange.svg)
![Status](https://img.shields.io/badge/status-development-yellow.svg)

This project implements a solution to the Virtual Machine (VM) bin packing problem using Mixed Integer Linear Programming (MILP). It optimizes the assignment of VMs to clusters while respecting resource constraints.

## Problem Description

The problem involves assigning virtual machines to clusters (bins) while respecting multiple resource constraints:
- vCPU capacity
- Memory (GB)
- Disk Space (GB)

The objective is to minimize the number of clusters used while ensuring all VMs are properly allocated.

## Features

- Random generation of VM configurations with realistic naming
- Random generation of cluster configurations with geographic naming
- Support for both relaxed and integer solutions
- Resource constraint handling for CPU, memory, and disk space
- Visualization of cluster assignments and resource utilization

## Dependencies

- numpy
- scipy

## Author

This project is developed by [@jovillios](https://github.com/jovillios).