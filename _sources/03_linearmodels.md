# Linear Models

1. (LM) Three data points are given as shown in the table, for which a linear model is built as
   
    $$\hat{y}=w_0+w_1 x $$

    | x | y |
    |---|---|
    | 1 | 1 |
    | 2 | 4 |
    | 3 | 9 |

    The value of $\left[\begin{array}{l}w_0 \\ w_1\end{array}\right]$, such that the squared error $(y-\hat{y})^2$ is minimum, is
     - $\left[\begin{array}{lcc} 3 & 6\\ 6&14\end{array}\right]^{-1}\left[\begin{array}{l}14 \\ 36\end{array}\right]$
     - $\left[\begin{array}{lcc}1 & 1 & 1 \\ 1 & 2 & 3\end{array}\right]\left[\begin{array}{l}1 \\ 4 \\ 9\end{array}\right]$
     - $\left[\begin{array}{lcc}2 & 3 & 4 \\ 3 & 5 & 7 \\ 4 & 7 & 10\end{array}\right]^{-1}\left[\begin{array}{l}1 \\ 4 \\ 9\end{array}\right]$
     - $\left[\begin{array}{lcc}1 & 1 & 1 \\ 1 & 2 & 3\end{array}\right]\left[\begin{array}{lcc}2 & 3 & 4 \\ 3 & 5 & 7 \\ 4 & 7 & 10\end{array}\right]^{-1}\left[\begin{array}{l}1 \\ 4 \\ 9\end{array}\right]$

2. (LM) For feature selection, a model $\hat{y}=\sum_i w_i x_i$ is trained in a way that many $w_i$ become zero. To achieve this, the regularization term that is added to the loss function is
     - $\Sigma_t\left|w_i\right|^2$
     - $\Sigma_t\left|w_i\right|$
     - $\Sigma_t\left|w_i\right|^{-1}$
     - $(y-\hat{y})^2$
     - None of these

3. (LM) A non-linear model $\hat{y}=\sigma\left(w_0+w_1 x\right)$ is to be optimized using gradient descent algorithm over the loss term $L=\frac{1}{2}(y-\hat{y})^2$. Here, $\sigma(\cdot)$ is the sigmoid function. The weights are chosen to be $w_0=\log _e(2), w_1=\log _e(0.5)$ . Learning rate $\eta=1$. Find the updated value of $w_0$ affer iterating once over the training data $(x=2, y=2 / 3)$.

      - $\ln(2)-\frac{1}{3}$
      - $\ln(2)-\frac{2}{27}$
      - $\ln(2)+\frac{1}{3}$
      - $\ln(2)+\frac{2}{27}$
      - None of these

4. (LM) $\tanh (x)=\frac{e^x-e^{-x}}{e^x+e^{-x}}$

The derivative of $\tanh (x)$ w.r.t. $x$ at $x=\ln 2$ is

      - 0.6
      - 0.64
      - 0.5
      - 0.75
      - None of these

1. (LM) For a model ${y}=A(x)w$, we need to optimize $w$ while $A$ is a known function. The training data is given as (x,t) and the error function to be minimized is 
$$E=(t-y)^T R (t-y) + \lambda w^T w$$
where $R$ is a given symmetric matrix. Here $y,x,w,t$ are vectors and $A,R$ are matrices.
The optimal $w$ is

Hint: Vector derivative formla from wikipedia: $\frac{\partial(u^T Av)}{\partial x} = \frac{\partial u}{\partial x} Av + \frac{\partial v}{\partial x} A^T u$, where $A$ is independent of $x$.
      - $(A^T RA+\lambda I)^{-1} A^T Rt$
      - $(A^T RA+\lambda I)^{-1} A^T t$
      - $A^T (ARA^T+\lambda I)^{-1} t$
      - $A^T (ARA^T+\lambda I)^{-1} Rt$
      - None of these

1. (LM) A linear model is built as $\hat{y}=w_0+w_1x+w_2x^2$. Given training data $\left(x,y\right)$ as $\left(0,3\right)$ and $\left(1,2\right)$, find the value of $\mathbf{w}=\left[w_0,w_1,w_2\right]$ such that $\left|y-\hat{y}\right|+\left|\mathbf{w}\right|^2$ is minimum.

2. (LM) A linear model is built as $\hat{y}=w_0+w_1x+w_2x^2$. Given training data $\left(x,y\right)$ as $\left(0,3\right)$ and $\left(1,2\right)$, find the value of $\mathbf{w}=\left[w_0,w_1,w_2\right]$ such that $\left|y-\hat{y}\right|^2+\left|\mathbf{w}\right|^2$ is minimum. 

3. (LM) $\hat{y}=ax+be^x$. Estimate $(a,b)$ using the training data $(x,y)$ as ${(1,2), (-1,6), (-0.5,3)}$ so as to minimize $\mathbb{E}[(y-\hat{y})^2]$. Write $a$ and $b$ upto one place of decimal.

4. (LM) A linear classifier to distinguish roses from lotuses is a line passing through points $(0,-5)$ and $(3,0)$ on the 2D Euclidean plane (length, width). The distance of a flower with size $(2,2)$ from this line is closest to
      - 1.3
      - 1.6
      - 1.9
      - 2.2
      - 2.5

5.  (LM) Consider a 3-class classification problem in which the loss incurred when an input vector from class $k$ is classified as belonging to class $j$ is given by the loss matrix 

    $$L_{kj}= \left[\begin{array}{ccc}0&4&1\\2&0&1\\2&1&0\end{array} \right].$$ 
  
    Draw the decision regions for the three classes on the plane whose axes are $p(c=0|x), p(c=1|x)$. 
