# LPCC

## Unit 4 Parsers

Q1. Construct parsing table for LL and LR parser using the following grammer

(Note: The grammer used here can vary but in exam only one grammer will be given)

    A. For LL parser

![LL parsing table](./images/LL%20parsing%20table%202.jpg "Title")

    B. For LR parser

![LL parsing table](./images/LR%20Parsing%20table.jpg "Title")

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

Goto: It is like a jump from one state of DFD to other. It is very essential as it is used in parsed table. It is written above the arrow 

    Grammar
    E -> E`
    E -> BB
    B -> cB | d
![LL parsing table](./images/DFD.jpg "Title")
![LL parsing table](./images/goto.jpg "Title")

Q5. Show/present various cononical item set (LR parsing table) for given grammer

![LL parsing table](./images/LR%20Parsing%20table.jpg "Title")
![LL parsing table](./images/moves%20LR.jpg "Title")

Q6. Stack implimentation of LL and LR parser

    For LR parser

![LL parsing table](./images/LR%20Parsing%20table.jpg "Title")
![LL parsing table](./images/moves%20LR.jpg "Title")

    For LL parser

    S -> aABb
    A -> c | epsilon
    B -> d | epsilon

![LL parsing table](./images/LL%20parsing%20example.jpg "Title")

## Unit 5 Semantic analysis
