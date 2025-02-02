# Decision Trees

(1. TREE)
A decision tree can be implemented in a code using if-else conditions.
To classify a flower into R, L or J, using two features height h and diameter d, the following decision tree is made:
```
if h>2:
   y=L
elif d<1.5:
   if h>1.2:
      y=J
   elif d<1:
      y=J
   else:
      y=R
else:
   y=R
```
- Draw the regions in the input space corresponding to the three classes
- Draw the decision tree (with nodes)

(2. TREE)
Input-output data on a node is given as follows. Find the threshold that maximizes the information gain if that node is split.

| $x$ | $y$ |
|:---:|:-----:|
| 100 |   R   |
| 110 |   R   |
| 115 |   R   |
| 135 |   R   |
| 121 |   L   |
| 138 |   L   |
| 142 |   L   |
|  90 |   J   |
|  95 |   J   |

(3. TREE)
A discrete random variable $x$ can take one of the $N$ distinct values. With 
$$p(x=i)=\alpha_i; i=1,...,N$$
Find the values of $\alpha_i$ so as to 
- maximize Shannon entropy of $x$
- maximize Gini impurity of $x$
- minimize Gini impurity of $x$

(4. TREE)
Input-output data on a node is given as follows. 
- Calculate the impurity of the node
- Find the threshold that maximizes the information gain if that node is split.

|  $x$ |     $y$    |
|:----:|:----------:|
| -0.8 | -0.7173561 |
| -0.5 | -0.4794255 |
|  0.2 | 0.19866933 |
|   1  | 0.84147098 |
|  1.7 | 0.99166481 |
|   2  | 0.90929743 |

