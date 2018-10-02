# Cartesian Products

For two sets:
|A X B| = |A| X |B|

For multiple sets:

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/166c653bb08f11c1627772e9534c85fc4ec4946f)

```
import itertools

A = {1, 2, 3}
B = {4, 5}

# Find cartesian product A X B and its size
cartesian_product = set([i for i in itertools.product(A, B)])
print("Ordered pairs in %s x %s:  " %(A,B))
for i in cartesian_product:
    print(i)
print("Size = %i" %len(cartesian_product))
```
Ordered pairs in {1, 2, 3} x {4, 5}:  

(1, 4)

(1, 5)

(2, 5)

(3, 4)

(2, 4)

(3, 5)

Size = 6

```
# |A X B| directly
print(len(cartesian_product))
```
6

```
# |A X B| using product rule
print(len(A)*len(B))
```
6
