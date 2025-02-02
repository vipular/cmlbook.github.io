# NN Optimization

1. (NNO) $y = \text{ReLU}\left(\sum_{i=0}^{1} v_i d_i\right)$ where $d_i$ is a dropout layer with a dropout probability of 0.2. If $v_i$ = [-0.4, 0.8] for $i$ = [0, 1], the expected value $E\left[ y \right]$ is ___.

2. (NNO) A network is to be trained to detect rose from input-target pairs (x,t). The final layer has one neuron with output \(h\) and final estimate $P(\text{Rose} | x; \theta) = \sigma(h)$ To train the network, binary cross entropy loss function is used, i.e., 
   
   $$\mathcal{L}(\theta) = -t \ln P(\text{Rose} | x; \theta) - (1 - t) \ln P(\text{not Rose} | x; \theta).$$ 
   
   Then $\frac{\partial \mathcal{L}(\theta)}{\partial \theta}$ is
    - $\left(\sigma\left(h\right)-t\right)\frac{\partial h}{\partial\theta}$
    - $\left(t-\sigma\left(h\right)\right)\frac{\partial h}{\partial\theta}$
    - $\left(\frac{t}{\sigma\left(h\right)}-\frac{1-t}{1-\sigma\left(h\right)}\right)\frac{\partial h}{\partial\theta}$
    - $\left(\frac{t}{\sigma\left(h\right)}+\frac{1-t}{1-\sigma\left(h\right)}\right) \frac{\partial h}{\partial\theta}$
    - None of the above


3. (NNO)  For a multi-class classification problem, a neural network is given as follows:
   $$h_{i_1} = \sum_{i_0=1}^{2} w_{i_0i_1} x_{i_0}$$
   $$v_{i_1} = \sigma(h_{i_1})$$
   $$h_{i_2}' = \sum_{i_1=1}^{3} w_{i_1i_2}' v_{i_1}$$
   $$y_{i_2} = \text{softmax}(h_{i_2}') $$
   Use categorical cross-entropy loss to compute the following:
   1. Write the loss function \(E\) in terms of the variables defined above and the targets $t_{i_2}$.
   2. $\frac{\partial E}{\partial y_1}$ (i.e., $i_2$ = 1).
   3. $\frac{\partial E}{\partial w_{11}'}$ (i.e., $i_1$ = $i_2$ = 1).
   4. $\frac{\partial E}{\partial w_{11}}$ (i.e., $i_0$ = $i_1$ = 1).

4. (NNO) The empirical risk over data d is written as $\mathcal{R}_d$. In the case of overfitting, the following happens during training
    - $\mathcal{R}_{train}$ does not decrease further
    - $\mathcal{R}_{val}$ does not decrease further and becomes constant
    - $\mathcal{R}_{train}$ decreases but $\mathcal{R}_{val}$ increases
    - $\mathcal{R}_{train}$ oscillates
    - $\mathcal{R}_{train}$ becomes constant due to parameters being stuck in a local minimum

5. (NNO) A recurrent neural network is given as 

    $$y_i^{\left(t\right)}=\sigma\left(\sum_{j}{u_{ij}x_j^{\left(t\right)}}+\sum_{j}{w_{ij}y_j^{\left(t-1\right)}}+b_i\right)$$

    The gradient $\frac{\partial y_i^{\left(t\right)}}{\partial b_i}$ is given by
    - $y_i^{\left(t\right)}\left(1-y_i^{\left(t\right)}\right)$
    - $y_i^{\left(t\right)}\left(1-y_i^{\left(t\right)}\right)\left(1+w_{ii}\right)$
    - $\sum_{l=0}^{\infty}{\left(\prod_{k=0}^{l}{y_i^{\left(t-k\right)}\left(1-y_i^{\left(t-k\right)}\right)}\right)w_{ii}^l}$
    - $\sum_{l=0}^{\infty}{\left(y_i^{\left(t-l\right)}\left(1-y_i^{\left(t-l\right)}\right)\right)w_{ii}^l}$
    - None of the above

6. (NNO) For feature selection, a model $\hat{y}=\sum_{i}{w_ix_i}$ is trained in a way that many $w_i$ become zero. To achieve this, the regularization term that is added to the loss function is
    - $\sum_{i}\left|w_i\right|^2$
    - $\sum_{i}\left|w_i\right|$
    - ${\sum_{i}\left|w_i\right|}^{-1}$
    - $\left(y-\hat{y}\right)^2$
    - None of the above

7. (NNO) $\tanh{\left(x\right)}=\frac{e^x-e^{-x}}{e^x+e^{-x}}$.
    The derivative of $\tanh(x)$ w.r.t. $x$ at $x=\log_e{2}$ is
   - 0.6
   - 0.64
   - 0.5
   - 0.75
   - None of the above
    
8. (NNO) A non-linear model $\hat{y}=\sigma(w_0+w_1x)$ is to be optimized using gradient descent algorithm over the loss term $\mathcal{L}=\frac{1}{2}\left(y-\hat{y}\right)^2$. Here, $\sigma\left(\cdot\right)$ is the sigmoid function. The weights are chosen to be $w_0=\log_e\ \left(2\right),\ w_1=\log_e\left(0.5\right)$. Learning rate $\eta=1$. Find the updated value of $w_0$ after iterating once over the training data $\left(x=2,y=2/3\right)$. 
   - $\log_e\ \left(2\right)-\frac{1}{3}$
   - $\log_e\ \left(2\right)-\frac{2}{27}$
   - $\log_e\ \left(2\right)+\frac{1}{3}$
   - $\log_e\ \left(2\right)+\frac{2}{27}$
   - None of these

9.  (NNO) The data for flower ($R$ or $L$) classification is given as 
   
   $$\mathbf{x}^{\intercal}=\left[\begin{matrix}5&4&5.5&2&3\\2&2.5&3&4.5&4\\\end{matrix}\right], \mathbf{y}^{\intercal}=[R,R,R,L,L].$$ 
   
   What is the first sample, i.e., $\mathbf{x}[0,:]$, after normalizing it to zero mean and unit variance (use MLE).
    - $[0.86,-1.3]$
    - $[0.27,-1.2]$
    - $[0,0]$
    - $[1.23,-1.32]$
    - None of these

10. (NNO) For multi-label classification, a neural network has 3 inputs. There is no hidden layer. The output layer has 2 neurons, $h_j=\sum_{i=1}^3 w_{ij} x_i + b_j$. If the target is $t_j$ and the model predicts $\hat{y}_j$, the update rule for $w_{ij}$ is:
    - $w_{ij} \leftarrow w_{ij}+\eta (t_j-\hat{y}_j)x_i$
    - $w_{ij} \leftarrow w_{ij}+\eta (\frac{t_j}{\hat{y}_j}-\frac{1-t_j}{1-\hat{y}_j})x_i$
    - $w_{ij} \leftarrow w_{ij}+\eta (\frac{t_j}{\hat{y}_j}-\frac{1-t_j}{1-\hat{y}_j})y_j x_i$
    - $w_{ij} \leftarrow w_{ij}+\eta (t_j\log\hat{y}_j)x_i$
    - $w_{ij} \leftarrow w_{ij}+\eta (t_j\log\hat{y}_j + (1-t_j)\log(1-\hat{y}_j))x_i$
    - None of these

11. (NNO) For hyperparameter tuning, which of the following is found to work best for large search spaces
    - Grid search with narrow grid
    - Grid search with wide grid
    - Gradient descent with adaptive stepsize
    - Pick randomly
    - Analytic optimization

12. (NNO)
   - What is Overfitting?
   - How would you detect if your model is overfitting?
   - What different methods could you use to avoid it?

