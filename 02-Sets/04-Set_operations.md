# Set Operations

There are several fundamental operations for constructing new sets from given sets. 
    Commutative laws:

            A ∪ B = B ∪ A 
            A ∩ B = B ∩ A 

   Associative laws:

            ( A ∪ B ) ∪ C = A ∪ ( B ∪ C ) 
            ( A ∩ B ) ∩ C = A ∩ ( B ∩ C ) 

   Distributive laws:

            A ∪ ( B ∩ C ) = ( A ∪ B ) ∩ ( A ∪ C ) 
            A ∩ ( B ∪ C ) = ( A ∩ B ) ∪ ( A ∩ C ) 
### Unions
Two sets can be "added" together. The union of A and B, denoted by A ∪ B, is the set of all things that are members of either A or B. The union of A and B, denoted by A ∪ B, is the set of all things that are members of either A or B. 

![](https://upload.wikimedia.org/wikipedia/commons/thumb/3/30/Venn0111.svg/220px-Venn0111.svg.png)

Examples:
  - {1, 2} ∪ {1, 2} = {1, 2}
  - {1, 2} ∪ {2, 3} = {1, 2, 3}
  - {1, 2, 3} ∪ {3, 4, 5} = {1, 2, 3, 4, 5}

##### Basic properties of union
  - A ∪ B = B ∪ A.
  - A ∪ (B ∪ C) = (A ∪ B) ∪ C.
  - A ⊆ (A ∪ B).
  - A ∪ A = A.
  - A ∪ U = U.
  - A ∪ ∅ = A.
  - A ⊆ B if and only if A ∪ B = B.
  
  
### Intersections 
A new set can also be constructed by determining which members two sets have "in common". The intersection of A and B, denoted by A ∩ B, is the set of all things that are members of both A and B. If A ∩ B = ∅, then A and B are said to be disjoint. 

![](https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Venn0001.svg/220px-Venn0001.svg.png)

Examples:
  - {1, 2} ∩ {1, 2} = {1, 2}.
  - {1, 2} ∩ {2, 3} = {2}.
  
##### Basic properties of intersecions
  - A ∩ B = B ∩ A.
  - A ∩ (B ∩ C) = (A ∩ B) ∩ C.
  - A ∩ B ⊆ A.
  - A ∩ A = A.
  - A ∩ U = A.
  - A ∩ ∅ = ∅.
  - A ⊆ B if and only if A ∩ B = A.
        
### Compliments 
 
Two sets can also be "subtracted". The relative complement of B in A (also called the set-theoretic difference of A and B), denoted by A \ B (or A − B), is the set of all elements that are members of A but not members of B. Note that it is valid to "subtract" members of a set that are not in the set, such as removing the element green from the set {1, 2, 3}; doing so has no effect.

In certain settings all sets under discussion are considered to be subsets of a given universal set U. In such cases, U \ A is called the absolute complement or simply complement of A, and is denoted by A′.

 A′ = U \ A

Examples:
  - {1, 2} \ {1, 2} = ∅.
  - {1, 2, 3, 4} \ {1, 3} = {2, 4}.
  - If U is the set of integers, E is the set of even integers, and O is the set of odd integers, then U \ E = E′ = O.

##### Basic properties of complements:
  - A \ B ≠ B \ A for A ≠ B.
  - A ∪ A′ = U.
  - A ∩ A′ = ∅.
  - (A′)′ = A.
  - ∅ \ A = ∅.
  - A \ ∅ = A.
  - A \ A = ∅.
  - A \ U = ∅.
  - A \ A′ = A and A′ \ A = A′.
  - U′ = ∅ and ∅′ = U.
  - A \ B = A ∩ B′.
  - if A ⊆ B then A \ B = ∅.
        
   The compliment of A in U
   
   ![](https://upload.wikimedia.org/wikipedia/commons/thumb/e/eb/Venn1010.svg/220px-Venn1010.svg.png)
