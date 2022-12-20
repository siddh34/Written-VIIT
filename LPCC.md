# LPCC

## Unit 4 Parsers

Q1. Construct parsing table for LL and LR parser using the following grammer

(Note: The grammer used here can vary but in exam only one grammer will be given)

    A. For LL parser

![LL parsing table](./images/LL%20parsing%20table%202.jpg "Title")

    B. For LR parser

![LR parsing table](./images/LR%20Parsing%20table.jpg "Title")

Q2. Check whether grammer is LR or LL grammer

**Note: (We will only show for LL the identification process remains the same for LR parser)*

![LL parsing table](./images/not%20LL%20grammar.jpg "Title")

Q3. First and Follow examples

    A. Computing First for:
    E -> TE’ 
    E’ -> + TE’ | epsilon
    T -> FT’ 
    T’ -> * FT’ | epsilon
    F -> ( E ) | id

    FIRST(E) = first(TE’) = first(T) =  first(FT’)   =first(F) ={(, id}
    First(E’) = {+, epsilon}
    First(T’) = {*, epsilon}

    B. Compute Follow for
    S -> aABb
    A -> c | epsilon
    B -> d | epsilon

    Follow(S) = {$} // as there is nothing on right of S
    Follow(A) = {d}
    Follow(B) = {b}

Q4. Closure and goto LR(0) parser example

Closure: It is nothing but a dot in augmented grammar. Example X = Y . K (It only tells that Y is parsed and K is not parsed. So the things on rigth side are not parsed)

Goto: It is like a jump from one state of DFD to other. It is very essential as it is used in parsed table. It is noted like from I0 state where it went.

    Grammar
    E -> E`
    E -> BB
    B -> cB | d
![LR parsing table](./images/DFD.jpg "Title")
![LR parsing table](./images/goto.jpg "Title")

Q5. Show/present various cononical item set (LR parsing table) for given grammer

![LR parsing table](./images/LR%20Parsing%20table.jpg "Title")
![LR parsing table](./images/moves%20LR.jpg "Title")

Q6. Stack implimentation of LL and LR parser

    For LR parser

![LR parsing table](./images/LR%20Parsing%20table.jpg "Title")
![LR parsing table](./images/moves%20LR.jpg "Title")

    For LL parser

    S -> aABb
    A -> c | epsilon
    B -> d | epsilon

![LL parsing table](./images/LL%20parsing%20example.jpg "Title")

Those who are having difficulty in LR parsing. Please watch

<https://youtu.be/MWX0-_mHYcc>

Q7.  What are parsers?

    1. It generates IR (Parse tree)
    2. Performs context-free syntax analysis and error correction
    3. Types of parsers
    A.Top-down
        a. Builds parse tree from root (top) to leaves (bottom)
        b. may require backtracking
        c. Includes Recursive Descent parser, Predictive parsers
    B. Bottom-up
        a. Builds parse tree from leaves (bottom) to root (up)
        b. As input is consumed, changes state to encode possibilities (recognize valid prefixes)
        c. Includes LR parser,LR parser

Q8. Find first and follow

    S → aBDh
    B → cC
    C → bC / ∈
    D → EF
    E → g / ∈
    F → f / ∈

    Answer

    First(S) = { a }
    First(B) = { c }
    First(C) = { b , ∈ }
    First(D) = { First(E) – ∈ } ∪ First(F) = { g , f , ∈ }
    First(E) = { g , ∈ }
    First(F) = { f , ∈ }

    Follow(S) = { $ }
    Follow(B) = { First(D) – ∈ } ∪ First(h) = { g , f , h }
    Follow(C) = Follow(B) = { g , f , h }
    Follow(D) = First(h) = { h }
    Follow(E) = { First(F) – ∈ } ∪ Follow(D) = { f , h }
    Follow(F) = Follow(D) = { h }

## Unit 5 Semantic analysis

Q1. Difference between syntax and parse trees

![diff between syntax and parse tree](./images/parsers%20vs%20snytaxs.jpg "Title")

Q2. Three address code (if-else)

    if (a > b) || (c > d) 
        then t = 1 
        else t = 0

![if else](./images/new%20if%20else.jpg "Title")

Q3. Three address code (expression)

![Syntax tree grammar](./images/three%20address%20code%20expr.jpg "Title")

Q4. Syntax tree using SDT or SDD

![Syntax tree grammar](./images/syntax%20tree%20grammar.jpg "Title")

![Syntax tree grammar](./images/syntax%20tree.jpg "Title")

Q5. Infix to postfix using SDT

    SDT for infix to postfix conversion of expression for given grammar :

    Grammar :

    E -> E + T { print(‘+’) }

    E -> E – T { print(‘-‘) }

    E -> T { }

    T -> id { print(‘id’) }

Q6. Explain L-attributes and S-attributes

    S-attributed:
        1. If every attribute is synthesized, then an SDT is called S-attributed
        2. If every attribute is synthesized, then an SDT is called S-attributed
        3. Example
        L => E n E => E1 + T E => T  T => T1 * F T => F F => ( E ) F => digit

    L-attributed:
        1. If an attribute of an SDT is synthesized or inherited with some restriction on inherited attributes, it can inherit values from left siblings only
        2. Attributes of this SDT are evaluated by depth-first
        3. Semantic actions are placed anywhere in RHS 
        4. X => ABC {B.P = X.P, B.P = A.P}

## Unit 6 Code Optimization

Q1. For a given TAC prepare basic blocks

![BB](./images/BB%20TAC.jpg "Title")

Q2. Generate machine code for experesion  ((a – b) – (c – d)) – (e – (f – (g – h)))

    Three address code
    o T1 = a- b
    o T2 = c – d
    o T3 = T1 – T2
    o T4 = g – h
    o T5 = f – T4
    o T6 = e – T5   
    o T7 = T3 – T6

    Machine code

    o MOV a, R0
    o SUB b, R0
    o MOV c, R1
    o SUB d, R1
    o SUB R0, R1
    o MOV f, R2
    o MOV g, R1
    o SUB h, R1
    o SUB R1, R2
    o MOV e, R1

Q3. Explain Peephole Optimization

    1. In We replace short sequence of target instructions with a shorter or faster sequence whenever possible
    2. Each improvement may create opportunities for additional improvements
    3. Peephole optimizations
        a. Constant folding
        b. Unreachable Code removal
        c. Flow control optimization
        d. Reduction in strength
        e. Algebraic simplification
    4. Example
        a. Few repeat code is removed from the main code

Q4. Explain Loop Optimization
    Loop Optimization includes
        a. Code motion
            Removing variables outside of the loop
            Example
            while (i <= limit - 2)
            becomes
            t := limit - 2
            while (i <= t)
        b. Induction variables
            The variable inside the loop is eliminated
            Example
            for(int i = 0; i < max; i++){
                result += 2;
            }
            becomes
            for(;result < max*2;result += 2){}
            return result;
        c. Reduction in strength
            Instead of variables constants are used
            example
            x = x + x
            becomes
            x = x*2

Q5. Which optimization can be done here?

![expr](./images/evaluation%20expr.jpg "Title")

    Answer: COMMON SUBEXPRESSION ELIMINATION

    1. Observe B5 and B6 block
    2. We are directly eliminating the useless expressions
    3. The array's number can be updated in block B5 and B6
    4. The final version should look like this:

![expr](./images/final%20opti.jpg "Title")

Q6. Explain the issues in code generator

    1. The issue of input 
        a. The code generation phase just proceeds on an assumption that the input is free from all syntactic and state semantic errors, the necessary type checking has taken place
    2. Issues in design
        a. Target program
            We can generate symbolic instructions and use the macro facilities of assemblers in generating code but it needs additional efforts
        b. Memory Management
            Mapping the names in the source program to the addressesof data objects is done by the code generator.  
            If mapping in not efficient then it affects the entire language
        c. Instruction selction
            Fast and best instructions to be selected for best functioning
        d. Register allocation issues
            Use of registers make the computations faster in comparison to that of memory, so efficient utilization of registers is important
