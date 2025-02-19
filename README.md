# Solving Combinatorial Optimisation Problems (COP) Using Quantum Algorithms 

The COP solved in this research are the Travelling Salesman Problem (TSP) and the Quadratic Assignment Problem (QAP). This repository contains the experimental code, input data and results obtained for the TSP and the QAP using the solution techniques:
- Quantum Approximation Optimisation Algorithm (QAOA)

which are documented in the conference proceedings titled [On the Computational Performance of IBM Quantum Devices Applied to Combinatorial Optimisation Problems](https://ieeexplore.ieee.org/abstract/document/9311605) and the preprint titled [An investigation of IBM Quantum Computing device performance on Combinatorial Optimisation Problems
](https://arxiv.org/abs/2107.03638).
These methods were applied to the COP and executed on the IBM quantum devices. 

## Repository Details
**Code**
- This folder contains the Jupyter Notebooks, which apply the two solution techniques  and QAOA, to the COP.

**Data**
- This folder contains the corresponding COP datasets
- For the TSP: 
    - The `Matrices.txt` file contains all the matrices that are used in the QAOA. The `readInData()` function reads the `.txt` file and outputs an array corresponding to each matrix.  
    - These datasets follow the [TSPLIB](http://elib.zib.de/pub/mp-testdata/tsp/tsplib/tsp/index.html) formatting convention. Furthermore, these datasets were randomly generated.
    - The `optimal.txt` file contains the initial starting point corresponding to the matrices used in the VQE and QAOA. The `optimal()` function reads the `.txt` file and outputs an array corresponding to each matrix's initial point. 
- For the QAP:
    - The datasets labelled `made*.csv` are randomly generated QAP instances, and the number correlates to the number of facilities in the problem (the dimensions of the two matrices in the CSV file). The format of the CSV files follows that of the datasets available in [QAPLIB](https://www.opt.math.tugraz.at/qaplib/).
    - The datasets in the VQE and QAOA folders are the initial points used in the warm start approach taken in the papers listed. Each initial point corresponds to the QAP instance of the same size referenced in the name.

**Results**
- This folder contains the results obtained to the COP using the QAOA. 
- The experimental results (found in detail in the below-listed papers) show that classical benchmarks have the best results in terms of success rate, feasibility and computational time on both COP. VQE performs better than QAOA on the small number of instances tested on all the metrics used.
- Classical algorithms perform better than the VQE in terms of computational time. The figure below illustrates that the performance of the various employed quantum devices are consistent in terms of computational time, with the simulator performing the best. Thus, there is no distinct correlation between problem size and computational time for quantum devices. However, this claim is made with a limited number of problem instances.
- Noisy intermediate-scale quantum (NISQ) devices' low reliability is attributed to the high variability in physical characteristics such as error rates and coherence time. These attributes substantiate why there lacks a distinct relationship between the problem size and the computational time required to find a solution using the VQE algorithm.


