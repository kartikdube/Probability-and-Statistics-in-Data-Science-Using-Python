# Sets
A set is a well-defined collection of distinct objects. The objects that make up a set (also known as the set's elements or members) can be anything: numbers, people, letters of the alphabet, other sets, and so on..

### Elements of a set
An element, or member, of a set is any one of the distinct objects that make up that set. 

Writing ![](https://wikimedia.org/api/rest_v1/media/math/render/svg/803f93dc0e1132de0c52ef8ef17b6c7224b05917) means that the elements of the set A are the numbers 1, 2, 3 and 4.

### Notation of sets
  
  - ![](https://wikimedia.org/api/rest_v1/media/math/render/svg/27bcc9b2afb295d4234bc294860cd0c63bcad2ca ) means that "x is an element of A
  - ![](https://wikimedia.org/api/rest_v1/media/math/render/svg/cff688698c6af2962bbfc3959fe6526ec3e76d20) meaning "A contains x"
  - ![](https://wikimedia.org/api/rest_v1/media/math/render/svg/8152431575305d6a6145adf9b279891a65923eba) means that "x is not an element of A"

```
# A set of numbers
set([1,2,30])
```
{1, 2, 30}

```
# order is not presenrved
# When printing out a set, the elements will be listed 
# A set of strings
set(['this','that','the other'])
```
{'that', 'the other', 'this'}

```
# each element can appear in a set only once.
set([1,2,3,2])
```
{1, 2, 3}

```
# Create an empty set
A = set()
# Add elements from a set
A = set()
A.update({0, 10})
print(A)
```
{0, 10}

```
# Delete an element from a set
A = {1, 2, 3}
A.remove(2)       # Works only if the element to be deleted is present in the set
A.discard(4)      # Works even if the element to be deleted is not present in the set
A.discard(3)      
print(A)
```
{1}

```
# Remove a random element from a set
A = {1, 2, 3}
A.pop()
print(A)
```
{2, 3}

```
A = {-1,2,1, 3}
A.pop()
print(A)
```
{2, 3, -1}

```
# Get a sorted list from a set
A = {1, 10, 4, -9, 7, 8, -6, 3, 2}
print(sorted(A))
```
[9, -6, 1, 2, 3, 4, 7, 8, 10]

### Elements of sets must be immutable in python

```
#elements can be tuples
set([(1,2),(1,3),(3,1)])
```
{(1, 2), (1, 3), (3, 1)}

```
# but cannot be lists
set([[1,2],[1,3],[3,1]])
```
**TyperError Traceback**
