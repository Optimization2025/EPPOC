# EPPOC
This repository contains the instances and code used in our paper "Fleet and Infrastructure Planning for Heavy-duty Electric Vehicles with Opportunity Charging".
## INTRODUCTION:
- Code supplement for the paper "Vessel Service Planning in Seaports".

## REQUIREMENTS:
- Linux Environment
- CPLEX 20.1.0 or higher (https://www.ibm.com/analytics/cplex-optimizer).
- See how to write C++ applications using CPLEX with Concert Technology (https://www.ibm.com/docs/en/icos/22.1.1?topic=users-creating-c-application-concert-technology). 

## DATASETS:
- The instance data are provided in the folder "data". 
- For a detailed explanation of the instance data, find the "README" file in the folder "data". 

## CODE:
- Code of all algorithms used in our computational experiments is provided in the folder "sourcecode". 
- List of .cpp files in the subfolder "src":
  1. BD1: the basic Benders decomposition algorithm outlined in EC.3.2 within a branch-and-cut framework.
  2. BD2：BD2 extends BD1 by incorporating Pareto-optimality cuts
  3. BD3: BD3 builds on BD2 by including lower-bound lifting inequalities and subproblem reduction trategies
  4. CPLEX_M1:  CPLEX on model M1 

## USAGE:
- To run an algorithm for solving an instance:
  1. Compile C++ project with CPLEX in Concert Technology;
  2. Load Selfmath.h and the .cpp file of the algorithm into the project;
  3. Copy the instance data from the "data" folder;
  4. Load the data into the code for the algorithm between lines "//input data starts here" and "//input data ends here";
  5. Build and run the code;
