# Disjoint Union

In set theory, the disjoint union (or discriminated union) of a family of sets is a modified union operation that indexes the elements according to which set they originated in. Or slightly different from this, the disjoint union of a family of subsets is the usual union of the subsets which are pairwise disjoint – disjoint sets means they have no element in common. 

example: 
  - {0} ∪ {1} = {0,1}
  - |Ac| = |Ω| - |A|
  - A ⊆ B -> B = A ∪ (B-A)
 
```
# Size of a set
NewSet = {1, 2}
print(len(NewSet))
```
2
```
# Smallest element in a set
NewSet = {2, 1, 3}
print(min(NewSet))
```
1
```
# Largest element in a set
NewSet = {-9, -1, -7}
print(max(NewSet))
```
-1
```
 Print the sum of elements of a set
A = {1, 5, 2, -10, 19}
print(sum(A))
```
17
```
# Verify the above using a 'for' loop
total=0
for i in A:
    total += i
print(total)
```
17
```
A = {1, 2, 3}
B = {1, 3, 5}
print(len(A),len(B))
```
3 3
```
# Intersection
C = A & B
print(C, "\n", len(C))
```
{1, 3} 
 2
 ```
 # Difference
E = A-B
print(E, "\n", len(E))
```
{2} 
 1
