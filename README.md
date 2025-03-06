# Sports League Scheduling Models

This repository contains several Jupyter notebooks implementing different Integer Programming (IP) formulations and heuristics for Single Round Robin (SRR) league scheduling. The source code was developed as part of the thesis *"Optimizing Sports League Scheduling: A Comparative Study of Integer Programming Approaches."*

## File Descriptions

1. **DevelopedHeuristic_Stages_1and2.ipynb**  
   - Implements the first stages of our proposed iterative heuristic.  
   - Generates an initial feasible set of home–away patterns.  
   - **Note:** Evaluated on an instance with 20 teams to illustrate efficiency versus other pattern-based methods.

2. **DevelopedHeuristic_Stages_3and4.ipynb**  
   - Continues from Stages 1 and 2.  
   - Incorporates advanced constraints (e.g., carry-over effect) and finalizes the schedule.

3. **Direct_Team_Pairing.ipynb**  
   - Implements a direct IP model that pairs teams each round.  
   - **Note:** Tested on a 10-team instance.

4. **Pattern-Based_Classical_Decomposition_Phase1.ipynb**  
   - Phase 1 of the classical decomposition approach, generating a feasible schedule of pattern pairings.  
   - **Note:** Run on a 10-team instance.

5. **Pattern-Based_Classical_Decomposition_Phase2.ipynb**  
   - Phase 2 of the classical decomposition approach, assigning teams to patterns.  
   - **Note:** Run on a 10-team instance.

6. **Pattern-Based_Integrated.ipynb**  
   - A fully integrated pattern-based model that includes all constraints in a single formulation.  
   - **Note:** Due to its exponential complexity, this model is demonstrated on a 6-team instance.

## How to Use

- **DevelopedHeuristic_Stages_1and2** → **DevelopedHeuristic_Stages_3and4:**  
  Run the first notebook to generate and validate feasible patterns, then feed its output into the second notebook to finalize the schedule under advanced constraints.

- **Pattern-Based_Classical_Decomposition_Phase1** → **Phase2:**  
  Use Phase 1 to build a schedule of pattern pairings, then run Phase 2 to assign teams to these patterns.

- **Direct_Team_Pairing** and **Pattern-Based_Integrated:**  
  These notebooks are standalone and can be run independently for performance comparisons.

## Requirements

- [Python 3.x](https://www.python.org/)  
- [Jupyter Notebook](https://jupyter.org/)  
- [Gurobi](https://www.gurobi.com/) (or another solver compatible with `gurobipy`)  
- Additional libraries as specified in each notebook.

## License and Citation

Feel free to adapt or extend these notebooks for research or practical scheduling applications. If you use this code, please cite the corresponding paper or thesis to acknowledge the original work.
