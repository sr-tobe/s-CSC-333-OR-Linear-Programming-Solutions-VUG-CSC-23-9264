Overview
This Python script provides solutions to multiple optimization problems using linear programming techniques. It is designed to demonstrate the application of linear programming to real-world scenarios such as maximizing profits, minimizing costs, and optimizing resource allocation.

Features
Implements linear programming using scipy.optimize.linprog.
Visualizes constraints and feasible regions with matplotlib.
Solves maximization and minimization problems.
Handles various use cases such as production planning, cost minimization, and resource allocation.
Dependencies
The script requires the following Python libraries:

NumPy: For numerical computations and data handling.
Matplotlib: For graphical visualization of constraints and feasible regions.
SciPy: For solving linear programming problems.
Install these dependencies using:

bash

pip install numpy matplotlib scipy
Script Structure
The script is divided into two main parts:

Function Definition:

solve_lp(objective, lhs_ineq, rhs_ineq, bounds, x_label, y_label, title): A generic function to solve linear programming problems and visualize constraints.
Parameters:
objective: Coefficients of the objective function.
lhs_ineq: Coefficients of the inequality constraints (left-hand side).
rhs_ineq: Right-hand side values for inequality constraints.
bounds: Bounds for the decision variables.
x_label, y_label, title: Labels for visualization.
Problem Definitions: Each problem is defined by its:

Objective function (maximization or minimization).
Constraints (inequalities).
Bounds for decision variables.
Descriptive labels for the decision variables.
Problem Scenarios
The script includes solutions to the following scenarios:

Maximizing Factory Profit: Maximize profit based on product constraints.

Minimizing Manufacturing Cost: Minimize cost while meeting production constraints.

Maximizing Production with Resource Constraints: Optimize production given limitations on labor, materials, and machine time.

Maximizing Sales Revenue: Optimize revenue by allocating resources between sales channels.

Resource Allocation for Projects: Allocate resources optimally between two projects.

Bakery Production Planning: Maximize profit from chocolate and vanilla cake production.

Minimizing Transport Costs: Optimize vehicle assignments for transportation to minimize costs.

Revenue Optimization for Products: Maximize revenue given constraints on labor, materials, and machinery.

Advertising Campaign Budget Allocation: Allocate an advertising budget across multiple platforms to maximize return.

Meal Planning for Cafeteria: Optimize meal preparation with limited ingredients.

Execution
Run the script in any Python environment:

bash

python CSC333-VUG-CSC-23-9264.py
The results will display:

Optimal values for decision variables.
Feasible regions and constraints visualized as graphs.
Customization
To add new problems:

Define the objective, lhs_ineq, rhs_ineq, and bounds.
Call the solve_lp function with appropriate labels and a descriptive title.
Example:

python

objective = [-2, -3]  # Maximize 2x1 + 3x2
lhs_ineq = [[1, 2], [2, 1]]  # Inequality constraints
rhs_ineq = [10, 8]
bounds = [(0, None), (0, None)]

solve_lp(objective, lhs_ineq, rhs_ineq, bounds, "x1", "x2", "Sample Problem")
