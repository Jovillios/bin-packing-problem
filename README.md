# VM Placement Optimization

## Project Overview

This project focuses on optimizing the placement of Virtual Machines (VMs) onto clusters (or servers) while minimizing the number of clusters used. The problem involves various constraints related to VM requirements, cluster capacities, and additional placement rules.

## Problem Definition

### **Input:**

- A set of VMs, each with specific requirements:
  - Number of vCPUs
  - RAM (GB)
  - Disk space (GB)
- A set of clusters with given capacities:
  - Number of vCPUs
  - RAM (GB)
  - Disk space (GB)

### **Output:**

- Minimized number of clusters used.

## Problem Variants & Constraints

We consider multiple variants of the VM placement problem:

1. **Affinity and Anti-affinity Rules:**

   - Some VMs should be placed together (affinity).
   - Some VMs must not share the same cluster (anti-affinity).
   - Only anti-affinities between specific VM pairs are considered.

2. **Cluster Characteristics:**

   - Clusters can be partially occupied or initially empty.
   - Clusters may have heterogeneous capacities (multiple types of servers).

3. **Splitting of VMs:**
   - VMs may be split across multiple clusters.
4. **VM Families and Criticality Levels:**
   - VMs belong to families, each with a criticality level (1, 2, or 3).
   - Levels 1 & 2 or levels 2 & 3 can be together, but not levels 1 & 3.

## Mathematical Formulation

A mathematical formulation for the simplest variant is proposed:

- Integer Linear Programming (ILP) or Mixed-Integer Programming (MIP) formulation.
- Solvable using optimization solvers (e.g., Pyomo with CBC or GLPK in Python).
- The simplest formulation provides a lower bound for more constrained variants.

## Solution Approaches

The problem is intentionally open-ended, and various approaches can be explored based on background and expertise:

- **Exact methods:** Using optimization solvers to compute lower bounds.
- **Heuristic methods:** Adapting First Fit, Best Fit, or other heuristic-based approaches.
- **Metaheuristics:** Evolutionary algorithms, simulated annealing, etc.

## Getting Started

### Prerequisites

- Python 3.8+
- Pyomo (for mathematical modeling)
- CBC or GLPK solver

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/vm-placement.git
   cd vm-placement
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run an example:
   ```bash
   python main.py
   ```

## Contributions

Contributions are welcome! Feel free to open issues or submit pull requests.

## Contact

If you have any questions or need further clarifications, feel free to reach out.

---

This project provides a flexible approach to VM placement optimization. Choose the methods that best fit your expertise and experiment with different solution techniques!
