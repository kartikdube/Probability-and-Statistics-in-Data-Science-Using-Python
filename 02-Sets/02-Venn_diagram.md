# Venn Diagrams

A Venn diagram (also called primary diagram, set diagram or logic diagram) is a diagram that shows all possible logical relations between a finite collection of different sets. Each set is represented by a circle. The
circle size represents the importance of the group. The groups are usually overlapping: the size of the overlap represents the intersection between both groups. It is unadvised to make Venn diagram with more than 3
groups because it would become hard to read. In python, Venn diagram are realised using the venn2 and venn3 function of the matplotlib library according to the number of group you have. See here for module installation.

```
# library
import matplotlib.pyplot as plt
from matplotlib_venn import venn2
 
# First way to call the 2 group Venn diagram:
venn2(subsets = (10, 5, 2), set_labels = ('Group A', 'Group B'))
plt.show()
 
# Second way
venn2([set(['A', 'B', 'C', 'D']), set(['D', 'E', 'F'])])
plt.show()
```
![](https://python-graph-gallery.com/wp-content/uploads/170_Basic_Venn_Diagram.png)
