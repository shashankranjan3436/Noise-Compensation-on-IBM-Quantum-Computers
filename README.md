# Noise-Compensation-on-IBM-Quantum-Computers
Quantum algorithms provide effective resolutions to computational issues that are difficult to solve using classical methods but can be solved efficiently using quantum computing techniques. The commercial use of quantum computing carries financial implications as it significantly impacts cryptography, a critical aspect of communication and information security businesses. This Report highlights a crucial matter concerning the performance gap between quantum circuits simulated on computers and those executed on actual quantum hardware. We specifically apply this performance comparison to Simon’s algorithm, which runs on currently available quantum computers. Firstly, we describe sources of noise in IBM quantum computers using a few examples of simple quantum circuits. Then, we introduce an example problem, Simon’s problem, that can be solved more efficiently with a quantum algorithm than a classical algorithm. Further, the algorithmic solution is detailed with the implementation and results of running the algorithm on physical quantum computers in comparison to simulations.
## Simon's Problem
Simon’s problem states that, given a function f that maps n-bit strings to n-bit strings, determine whether f is a one-to-one function (i.e., each input maps to a unique output) or a two-to-one function (i.e., there exist two different inputs that map to the same output). Classically, the best algorithm for solving this problem requires O(2ˆ(n/2)) evaluations of the function, which is exponential in the size of the input. However, using a quantum computer and a specific algorithm called Simon’s algorithm, the problem can be solved in O(n) evaluations of the function. This represents an exponential speedup over classical algorithms. 
The problem that Simon’s algorithm is designed to solve is the following: given a function f :
{0, 1}
n → {0, 1}
n that is guaranteed to be "periodic" (i.e., there exists a bit string s ∈ {0, 1}
n
such that f(x) = f(x ⊕ s) for all x ∈ {0, 1}
n), find the string s. This problem has important
applications in cryptography, where it is used to break certain types of encryption schemes.
The classical approach to solving this problem involves evaluating the function f for 2
n−1 + 1
different inputs and using these evaluations to construct a system of linear equations that can be
solved to find s. However, this approach is inefficient for large n
