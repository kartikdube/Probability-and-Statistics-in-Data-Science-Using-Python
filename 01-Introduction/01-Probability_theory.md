# Probability Theory

Probability Theory is mathematical framework for comouting the probability of complex events. Uner the assumption that we know the probabilities of the basic events.

##### Example

We all know that if one flips a fair coin then the outcome is "heads" or "tails" with equal probabilities. It means that if we flip the coin k times, for some large value of k, say k = 10,000. 

Then the number of "heads" is about k/2 = 10,000/2 = 5,000

Instead of "Heads" and "Tails" we will use ![](http://latex.codecogs.com/png.latex?x_%7Bi%7D%20%3D%20-1%20%2C%20x_%7Bi%7D%20%3D%201%20%2C%20S_%7B10000%7D%20%3D%20x_%7B1%7D%20&plus;%20x_%7B2%7D%20&plus;....x_%7B10000%7D)

If the number of heads is about 5,000 then  ![](http://latex.codecogs.com/png.latex?S_%7B10000%7D%20%5Capprox%200)

```
import random
import numpy
import matplotlib.pyplot as plt

def generate_counts(k=1000,n=100):
    X=2*(numpy.random.rand(k,n)>0.5)-1  #generate a kXn matrix of +-1 random numbers
    S=sum(X,0) 
    return S
```
```
k=1000
n=1000
Grph = generate_counts(k=k,n=n)
fig = plt.figure(figsize=[10,4])
nsssss, bins, patches = plt.hist(Grph)
plt.xlim([-k,k])
plt.xlabel("sum")
plt.ylabel("count")
plt.title("Histogram of coin flip sum when flipping a coin %d times"%k)
plt.grid(True)
plt.show()
```
![](/Images/t1c1.png)

Note that the sum ![](http://latex.codecogs.com/png.latex?S_%7B10000%7D) is not exactly 0, it is only close to 0.

Using probability theory we can calculate how small is ![](http://latex.codecogs.com/png.latex?%5Cleft%20%7C%20S_%7Bk%7D%20%5Cright%20%7C)

```
from math import sqrt
k=1000
n=1000
fig = plt.figure(figsize=[13,3.5])
for j in range(2,5):
    k=10**j
    counts=generate_counts(k=k,n=100)
    plt.subplot(130+j-1)
    plt.hist(counts,bins=10);
    plt.xlim([-k,k])
    d=4*sqrt(k)
    plt.plot([-d,-d],[0,30],'r')
    plt.plot([+d,+d],[0,30],'r')
    plt.grid(True)
    plt.title('%d flips, bound=+-%6.1f'%(k,d))
    plt.show()
```
![](/Images/t1c2.png)

We observer that ![](http://latex.codecogs.com/png.latex?%5Cleft%20%7C%20S_%7Bk%7D%20%5Cright%20%7C) = ![](http://latex.codecogs.com/png.latex?4%5Csqrt%7Bk%7D) , which is smaller than ![](http://latex.codecogs.com/png.latex?2*10%5E%7B-8%7D) which is 0.000002%.

So, ![](http://latex.codecogs.com/png.latex?%5Cleft%20%7C%20S_%7Bk%7D%20%5Cright%20%7C) is almost always in range of [-![](http://latex.codecogs.com/png.latex?4%5Csqrt%7Bk%7D),+![](http://latex.codecogs.com/png.latex?4%5Csqrt%7Bk%7D)]

