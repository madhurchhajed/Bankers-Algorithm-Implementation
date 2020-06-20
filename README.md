# Bankers-Algorithm-Implementation
Banker’s Algorithm is a resource allocation and deadlock avoidance algorithm.

The Banker algorithm, sometimes referred to as the detection algorithm, is a resource allocation and deadlock avoidance algorithm 
developed by Edsger Dijkstra that tests for safety by simulating the allocation of predetermined maximum possible amounts of all 
resources, and then makes an "s-state" check to test for possible deadlock conditions for all other pending activities, before
deciding whether allocation should be allowed to continue. 

Procedure: 
1. Input: 
We need input for no. of resources and procedures from user. Then, we need three matrices from user for allocation matrix,
max matrix and available matrix.  

* Allocation Matrix: instances allocated to process 
* Max Matrix: Maximum instances required by process 
* Available Matrix: Matrix available for resources 

2. Process: 
First, we will create a need matrix, this matrix will show us instances of resources needed more by process.  
- Need Matrix = Max Matrix – Allocation Matrix 

Then, for every process we need to compare every instance of need matrix with every consecutive instance of available matrix. 
If every pair of need matrix instance is less or equal to instance of available matrix, then only we will allocate resource to 
that process. And hence, the process will be done.  

Need Matrix <= Available Matrix 

At last if all instances of need matrix are less than equal to available matrix, then only process will run.  
Then as the process ends, new available resources will be assigned.  

- New Available Matrix = Allocation Matrix + Available Matrix 


3. Output :
, Safe Sequence of Process 
