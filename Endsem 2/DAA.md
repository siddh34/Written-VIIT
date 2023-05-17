# DAA Important Questions

#### Unit 4 : Intractable Problems and NP-Completeness

1. Define and Explain P, NP, NP Complete and NP Hard.

   For Answer visit:

   1. [https://www.geeksforgeeks.org/types-of-complexity-classes-p-np-conp-np-hard-and-np-complete/](https://www.geeksforgeeks.org/types-of-complexity-classes-p-np-conp-np-hard-and-np-complete/)
2. What is deterministic and non-deterministic algorithm?

   For Answer visit:

   1. [https://www.tutorialspoint.com/difference-between-deterministic-and-non-deterministic-algorithms](https://www.tutorialspoint.com/difference-between-deterministic-and-non-deterministic-algorithms)
   2. [https://www.geeksforgeeks.org/difference-between-deterministic-and-non-deterministic-algorithms/](https://www.geeksforgeeks.org/difference-between-deterministic-and-non-deterministic-algorithms/)
3. Explain what is SAT Problem, prove 3-SAT is NP Complete.

   For Answer visit:

   1. [https://en.wikipedia.org/wiki/Boolean_satisfiability_problem](https://en.wikipedia.org/wiki/Boolean_satisfiability_problem)
   2. [Proof that SAT is NP Complete - GeeksforGeeks](https://www.geeksforgeeks.org/proof-that-sat-is-np-complete/)

   *To prove that 3-SAT is NP-complete, we need to show two things:*

   *(1) 3-SAT is in the class NP, and (2) any problem in NP can be reduced to 3-SAT in polynomial time.*

   1. *3-SAT is in NP:
      The class NP consists of decision problems for which a "yes" instance can be verified in polynomial time. In the case of 3-SAT, given a set of clauses, we can easily verify whether there exists an assignment of truth values to the variables that satisfies all the clauses. We can do this by simply checking each clause and confirming that at least one literal in each clause evaluates to true. This verification process can be done in polynomial time, so 3-SAT is in NP.*
   2. *Reduction of any problem in NP to 3-SAT:
      To show that any problem in NP can be reduced to 3-SAT, we will use a known NP-complete problem called CIRCUIT-SAT, which involves determining whether a Boolean circuit with AND, OR, and NOT gates can evaluate to true. We will show a polynomial-time reduction from CIRCUIT-SAT to 3-SAT, which will establish the NP-completeness of 3-SAT.*

   *Given an instance of CIRCUIT-SAT, we need to construct an equivalent instance of 3-SAT. We will focus on constructing a 3-SAT formula that is satisfiable if and only if the original Boolean circuit is satisfiable.*

   *To do this, we can represent each gate in the circuit as a clause in 3-SAT. We introduce variables to represent the outputs of each gate and add clauses that ensure the correct behavior of each gate.*

   1. *AND gate:
      For an AND gate with inputs x and y and output z, we introduce three new variables u, v, and w. We add the following clauses to the 3-SAT formula:
      (~x ∨ ~y ∨ u) and (x ∨ ~u) and (y ∨ ~u) and (~u ∨ ~v ∨ w) and (u ∨ ~w) and (v ∨ ~w)*
   2. *OR gate:
      For an OR gate with inputs x and y and output z, we introduce three new variables u, v, and w. We add the following clauses to the 3-SAT formula:
      (x ∨ y ∨ ~u) and (~x ∨ u) and (~y ∨ u) and (u ∨ ~v ∨ ~w) and (~u ∨ w) and (~v ∨ w)*
   3. *NOT gate:
      For a NOT gate with input x and output z, we add the clause (x ∨ z) to the 3-SAT formula.*

   *We also add clauses that enforce the correct behavior of the inputs and outputs of the circuit.*

   *Finally, we add a clause that requires at least one output variable to be true to ensure that the circuit evaluates to true. This clause is simply the disjunction of all the output variables.*

   *By constructing the 3-SAT formula in this way, we have a polynomial-time reduction from CIRCUIT-SAT to 3-SAT. Therefore, 3-SAT is NP-complete.*

   *Since we have shown that 3-SAT is in NP and any problem in NP can be reduced to 3-SAT, we have established the NP-completeness of 3-SAT.*
4. Explain CDP and prove CDP is NP Complete.

   For Answer visit:

   1. [Clique problem - Wikipedia](https://en.wikipedia.org/wiki/Clique_problem)
   2. [Proof that Clique Decision problem is NP-Complete - GeeksforGeeks](https://www.geeksforgeeks.org/proof-that-clique-decision-problem-is-np-complete/)
5. Show Hamiltonian Cycle problem in NP Complete

   For Answer visit

   1. [https://www.geeksforgeeks.org/proof-that-hamiltonian-cycle-is-np-complete/](https://www.geeksforgeeks.org/proof-that-hamiltonian-cycle-is-np-complete/)

#### Unit 5 : Approximation and Randomized Algorithms, Natural Algorithms

1. Explain what approximation is.
2. Solve TSP using approximation.
3. Explain the steps in genetic Algorithm explain them with example
4. Compare regular quick sort with randomized quicksort.
5. Explain Simulate annealing algorithm.

#### Unit 6 : Parallel and Concurrent Algorithms

1. Explain Amdahl's Law and Brent's Theorem
2. Write the formula for efficiency and speedup in parallel algorithm.
3. What is Work Optimal algorithm?
4. List and explain parallel models of programming (EREW,ERCW,CREW,CRCW)
5. Explain dining philosopher problem
