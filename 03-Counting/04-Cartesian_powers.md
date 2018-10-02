# Cartesian Powers

Cartesian product of a set with itself is a cartesian power.

For two sets:
X^2 = X × X

For multipple sets:

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/d31c44c67052aed5ae0d3865240381b2dff2eefe)

```
A = {1, 2, 3}
k = 2
```
```
# Print k'th cartesian power of A
print(set(itertools.product(A, repeat = k)))
```
{(1, 2), (3, 2), (1, 3), (3, 3), (3, 1), (2, 1), (2, 3), (2, 2), (1, 1)}
```
# Find |A|^k directly
print(len(A)**k)
```
9

Next we calculate and graph the exponential 2x2x and the polynomials xx and x2x2. We see that the exponential grows much faster than the polynomials.

```
import matplotlib.pyplot as plt
import numpy as np
import ipywidgets as widgets

def f(x_max):
    x = np.arange(0, x_max, 0.01)
    plt.plot(x, x, 'b', linewidth = 3, label = '$x$')
    plt.plot(x, x**2, 'r', linewidth = 3, label = '$x^2$')
    plt.plot(x, 2**x, 'm', linewidth = 3, label = '$2^x$')
    plt.xlabel('x', fontsize = 20)
    plt.xticks(fontsize = 18)
    plt.yticks(np.linspace(max(2**x_max, x_max**2)/10, max(2**x_max, x_max**2), 10), fontsize = 18)
    plt.gca().set_xlim([0, x_max])
    plt.gca().set_ylim([0, max(2**x_max, x_max**2)])
    plt.gcf().set_size_inches(20, 10)
    plt.legend(fontsize = 20)
    plt.show()
    
widgets.interact(f, x_max=widgets.FloatSlider(min = 0.5, max = 20, step = 0.5))
```
![](/Images/t3c2.png)

![](/Images/t3c3.png)
