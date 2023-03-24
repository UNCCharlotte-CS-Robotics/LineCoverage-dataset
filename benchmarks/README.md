Author: Saurav Agarwal (https://www.saurav.fyi/)

The file SRLCresults50cities.csv contains computation times and coverage tour costs for several single robot line coverage algorithms. These algorithms are tested on the most populous 50 cities road network dataset extracted from OpenStreetMap.

The algorithms are described in the following papers:

> The Single Robot Line Coverage Problem: Theory, Algorithms and Experiments  
> Agarwal S and Akella S (2020)  
> In: arXiv preprint arXiv:2208.09861 (2022).

> Approximation algorithms for the single robot line coverage problem.  
> Agarwal S and Akella S (2020)  
> In: Algorithmic Foundations of Robotics XIV. Oulu, Finland, pp. 534–550.


The algorithms are implemented in C++ and executed on a desktop computer with an Intel Core i9-7980XE processor. The ILP formulation is executed using Gurobi (https://www.gurobi.com/). The implementation can be found in the following GitHub repository:  
https://github.com/UNCCharlotte-CS-Robotics/LineCoverage-library

Description of columns of the file SRLCresults50cities.csv is given below.

Name: Name of the city  
NumVertices: Number of vertices in the road network graph  
NumRequiredEdges: Number of required edges. Required edges correspond to the road network line segments  
NumNonRequiredEdges: Number of non-required edges---a non-required edge is added between each pair of vertices, except for the pairs for which a required edge already exists.  
Length-meters: Total length of the required edges in meters based on real-world geographic information obtained from OpenStreetMap  
NumConnectedComponents: Number of connected components in the input graph  
ILP-ComputationTime-hours: Computation time required for the ILP formuation in hours   
ILP-TourCost: Cost of coverage tour generated using the ILP formulation  
b2a-time-s: Computation time for the Beta2-ATSP algorithm in seconds  
b2a-cost: Cost of coverage tour generated using the Beta2-ATSP algorithm  
b2a2-time-s: Computation time for the Beta2-ATSP with 2-opt heuristic in seconds  
b2a2-cost: Cost of coverage tour generated using the Beta2-ATSP with 2-opt heuristic algorithm  
b2g-time-s: Computation time for the Beta2-GTSP algorithm in seconds  
b2g-cost: Cost of coverage tour generated using the Beta2-GTSP algorithm  
b2g2-time-s: Computation time for the Beta2-GTSP with 2-opt heuristic algorithm in seconds  
b2g2-cost: Cost of coverage tour generated using the Beta2-GTSP with 2-opt heuristic algorithm  
b3a-time-s: Computation time for the Beta3-ATSP algorithm in seconds  
b3a-cost: Cost of coverage tour generated using the Beta3-ATSP algorithm  
b3a2-time-s: Computation time for the Beta3-ATSP with 2-opt heuristic algorithm  
b3a2-cost: Cost of coverage tour generated using the Beta3-ATSP with 2-opt heuristic algorithm  
