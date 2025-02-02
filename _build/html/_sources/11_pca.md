# Principal Component Analysis

(1.PCA) Find the eigen values of matrix  
$$A = \begin{bmatrix}
    3 & -1 \\
    -1 & 5 \\
\end{bmatrix}$$
<br>

(2.PCA) 2D data samples are given as $[(0,5.1), (2,5.8), (4,7.3), (6,8.5), (8,8.1)]$.
-  Plot the points and their PCA projections to 1D in the 2D plane.
-  Write the reduced representations for those points after dimensionality reduction.

(3.PCA) PCA is performed on 2D data $\{\bm x_n\}_{n=1}^N$ and the data is projected along the unit vector $[-1/\sqrt{2},1/\sqrt{2}]$. The mean vector of the original data is $[1,1]$. 
   - i. Consider $\bm x_1=[5,-3]$. Plot on 2D space $\bm x_1$ and its PCA projection $\bm x_1'$.
   - ii. What is $|\bm x_1-\bm x_1'|^2$?

## DTW
(1.DTW)
Align the two time series using DTW: $[0, 0,1, 1.5, 1.7, 0.5, 0]$ and $[0, 1.1, 1.5, 0.7, 0, 0, 0]$.

(2. DTW)
A field is represented by a 2D matrix, with each cell indicating the amount of crop that can be collected from that location.
$$\begin{bmatrix}
  16 & 14 & 11 &  5 & 23 &  6 & 25\\
  18 & 17 & 21 & 12 & 20 &  0 & 20\\
  21 & 13 & 13 &  7 &  3 & 18 & 15\\
  11 & 20 &  4 & 16 & 19 & 18 & 10\\
   1 & 16 & 16 & 24 &  0 & 24 & 11\\
   8 &  8 & 16 & 20 & 11 & 14 & 12
\end{bmatrix}$$
Assume a farmer starts from any cell in the first column and stops in the last column. He can only move right, diagonally right-up and diagonally right-down. Find the best path so that he collects maximum amount of crop in a single pass.
  - Write the cumulative score matrix along with the path links
  - Trace the best path.
  - Write the total amount of crop collected along the best path.
