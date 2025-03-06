# Sports League Scheduling Models

This repository contains several Jupyter notebooks implementing different Integer Programming (IP) formulations and heuristics for Single Round Robin (SRR) league scheduling. The files include the source code for the integer programming formulations developed as part of the thesis "Optimizing Sports League Scheduling: A Comparative Study of Integer Programming Approaches."

## File Descriptions

1. **DevelopedHeuristic_Stages_1and2.ipynb**  
   - First part of the proposed iterative heuristic.  
   - Generates an initial feasible set of home–away patterns in a sustainable manner (Stage 1) and confirms feasibility (Stage 2).  
   - The resulting feasible patterns are passed on to the next notebook.

2. **DevelopedHeuristic_Stages_3and4.ipynb**  
   - Continues from the output of the Stages 1 and 2 notebook.  
   - Incorporates advanced constraints (e.g., carry-over effect) and finalizes the schedule.  
   - Demonstrates how the reduced solution space approach can outperform classical methods as league size grows.

3. **Direct_Team_Pairing.ipynb**  
   - Implements an intuitive IP model that directly pairs teams in each round.  
   - Typically offers polynomial complexity and achieves optimal solutions with moderate computational effort.

4. **Pattern-Based_Classical_Decomposition_Phase1.ipynb**  
   - Phase 1 of the classical decomposition approach: produces a feasible schedule of pattern pairings.  
   - The generated schedule (patterns vs. patterns) feeds into Phase 2 for final team assignment.

5. **Pattern-Based_Classical_Decomposition_Phase2.ipynb**  
   - Phase 2 of the classical decomposition approach: assigns teams to the pattern schedule from Phase 1.  
   - Completes the two-step method widely referenced in scheduling literature.

6. **Pattern-Based_Integrated.ipynb**  
   - A single, integrated pattern-based model that includes all constraints (home–away sequences, fairness, COE) in one formulation.  
   - Comprehensive but potentially expensive for larger leagues due to exponential growth in variables and constraints.

## How to Use

- **DevelopedHeuristic_Stages_1and2** → **DevelopedHeuristic_Stages_3and4**:  
  Run the first notebook to generate and validate feasible patterns, then pass its output to the second notebook for final scheduling under carry-over constraints.

- **Pattern-Based_Classical_Decomposition_Phase1** → **Pattern-Based_Classical_Decomposition_Phase2**:  
  Use Phase 1 to build a pattern pairing schedule. Feed that schedule into Phase 2 to complete the assignment of teams to patterns.

- **Direct_Team_Pairing** and **Pattern-Based_Integrated**:  
  These are standalone notebooks that illustrate alternative IP approaches. Run them independently to compare their performance against the decomposition or heuristic methods.

## Requirements

- [Python 3.x](https://www.python.org/)  
- [Jupyter Notebook](https://jupyter.org/)  
- [Gurobi](https://www.gurobi.com/) (or another solver compatible with `gurobipy`)  
- Any additional libraries (e.g., `numpy`) may be specified at the top of each notebook.

## License and Citation

Feel free to adapt or extend these notebooks for research or practical scheduling. If you publish results using this code, please cite the corresponding paper or thesis to acknowledge the original work.
