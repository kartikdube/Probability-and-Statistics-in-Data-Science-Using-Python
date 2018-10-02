# Cartesin Product

In set theory (and, usually, in other parts of mathematics), a Cartesian product is a mathematical operation that returns a set (or product set or simply product) from multiple sets. That is, for sets A and B, the Cartesian product A × B is the set of all ordered pairs (a, b) where a ∈ A and b ∈ B. Products can be specified using set-builder notation, e.g. 
A table can be created by taking the Cartesian product of a set of rows and a set of columns. If the Cartesian product rows × columns is taken, the cells of the table contain ordered pairs of the form (row value, column value).

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/bcb60e49395e0c13e866a0bcf98dc0975802a57f)

![](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Cartesian_Product_qtl1.svg/220px-Cartesian_Product_qtl1.svg.png)

```
from itertools import product
test = {1, 2, 3}
list(powerset(test))
```
[(), (1,), (2,), (3,), (1, 2), (1, 3), (2, 3), (1, 2, 3)]
```
list(product(test, test))
```
[(1, 1), (1, 2), (1, 3), (2, 1), (2, 2), (2, 3), (3, 1), (3, 2), (3, 3)]
