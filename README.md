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
- Detailed computational results are provided in the folder "Detailed Results".

## CODE:
- Code of all algorithms used in our computational experiments is provided in the folder "src".
- All algorithms are for instances with fleet homogeneity requirements, i.e., \Gamma=1; for solving instances without fleet homogeneity requirements, please remove the following block from the code:
- 		{ 
			for (int f=1;f!=F;++f){
				for (int h=0;h!=H;++h){
					int index=FHindex[f][h];
					model.add(x[index]==0);	
				}
			}
			IloExpr sum(env); 
			for (int h=0;h!=H;++h){
				int index=FHindex[F][h];
				sum+=x[index];
			}
			model.add(sum==1);	
			sum.end();
		}
- List of subfolders in the folder "src":
  1. D100: This subfolder contains the codes of the Benders decomposition algorithms for solving instances with \Delta=0%
  2. D105: This subfolder contains the codes of the Benders decomposition algorithms for solving instances with \Delta=5%
- List of .txt files in the folders "src", "D100", and "D105": 
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
