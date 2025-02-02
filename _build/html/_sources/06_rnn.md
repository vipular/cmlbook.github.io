# Recurrent Neural Networks

1. (RNN) A recurrent layer with 10 units (neurons) operates on an input vector of length 5. Each unit has a sigmoid activation. The number of trainable parameters in this layer is ____.

2. (RNN) An RNN is given as $${\mathbf{h}}^{(t)} =U{\mathbf{x}}^{(t)} +W{\mathbf{h}}^{(t-1)}+ {\mathbf{b}}$$ $${\mathbf{\hat{y}}}^{(t)}=\text{softmax}({\mathbf{h}}^{(t)})$$ 
Here $\mathbf{x}$ and $\mathbf{\hat{y}}$ are vectors of length $N$. The model is trained for classification, with ${\mathbf{y}}^{(t)}$ as the one-hot target. Write the update equation for each element of $W$ matrix. Unroll for 3 time steps (till $t-3$).