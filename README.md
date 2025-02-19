Solving Combinatorial Optimisation Problems (COP) Using Quantum Algorithms
The COP solved in this research are the Travelling Salesman Problem (TSP) and the Quadratic Assignment Problem (QAP). This repository contains the experimental code, input data and results obtained for the TSP and the QAP using the solution techniques:


Quantum Approximation Optimisation Algorithm (QAOA)
which are documented in the conference proceedings titled On the Computational Performance of IBM Quantum Devices Applied to Combinatorial Optimisation Problems and the preprint titled An investigation of IBM Quantum Computing device performance on Combinatorial Optimisation Problems . These methods were applied to the COP and executed on the IBM quantum devices.

Repository Details
Code

This folder contains the Jupyter Notebooks, which apply the two solution techniques VQE and QAOA, to the COP.
Data

This folder contains the corresponding COP datasets
For the TSP:
The Matrices.txt file contains all the matrices that are used in the VQE and the QAOA. The readInData() function reads the .txt file and outputs an array corresponding to each matrix.
These datasets follow the TSPLIB formatting convention. Furthermore, these datasets were randomly generated.
The optimal.txt file contains the initial starting point corresponding to the matrices used in the VQE and QAOA. The optimal() function reads the .txt file and outputs an array corresponding to each matrix's initial point.
For the QAP:
The datasets labelled made*.csv are randomly generated QAP instances, and the number correlates to the number of facilities in the problem (the dimensions of the two matrices in the CSV file). The format of the CSV files follows that of the datasets available in QAPLIB.
The datasets in the VQE and QAOA folders are the initial points used in the warm start approach taken in the papers listed. Each initial point corresponds to the QAP instance of the same size referenced in the name.

