# Neural Networks (Dense)

1. (NN) The following code uses a sequential model from the Keras library. Find the total number of weights to be trained, including the biases.
```python
model.add(Dense(24, input-dim=100, activation='relu'))
model.add(Dense(2, activation='softmax'))
```

2. (NN) 
Given a model as 
$$y=g(Wx+b)$$
where g is given as $$g(x)=\begin{cases}x, & x>0 \\ 0.1x, & \text{otherwise.}\end{cases}$$ 
If $W=\left[\begin{array}{cc}2&1\\-2&1\end{array} \right]$, $b=\left[\begin{array}{c}1\\-1\end{array} \right]$ $x=\left[\begin{array}{c}0.5\\1\end{array} \right]$. Find $y_0$ and $y_1$, the two elements of $y$ vector.

3. (NN) 
Given a model as 
$$y=g(Wx+b)$$
where g is given as $$g(x)=\begin{cases}x, & x>0 \\ 0.1x, & \text{otherwise.}\end{cases}$$ 
If $W=\left[\begin{array}{cc}2&1\\-2&1\end{array} \right]$, $b=\left[\begin{array}{c}1\\-1\end{array} \right]$ $x=\left[\begin{array}{c}0.5\\1\end{array} \right]$. Find $\frac{\partial{y_i}}{\partial{w_{ij}}}$. Write its value for $(i,j)=[(0,0),(0,1),(1,0),(1,1)]$, respectively.

4. (NN) A model is defined as
```python
model = tf.keras.Sequential([
    tf.keras.layers.Dense(10, activation='relu'),
    tf.keras.layers.Dense(10, activation='relu'),
    tf.keras.layers.Dense(3, activation='softmax')
  ])
```
If the input is a vector of length 10, what is the total number of trainable parameters (including biases) in the model?

5. (NN) 
A neural network is used for regression. Which of the following statements are typically correct?
- The hidden layers can have tanh nonlinearity
- The output layer can have sigmoid nonlinearity
- The hidden layers can have softmax nonlinearity
- The output layer can have softmax nonlinearity 
- Binary cross entropy loss function can be used for training 
- Categorical cross entropy loss function can be used for training 
- The number of output neurons should be 1

6. (NN) Given a $[5,6,6,3]$ neural network (5 input neurons, 6 neurons in hidden layer 1, 6 neurons in hidden layer 2, 3 output neurons), the number of learnable parameters (weights and biases) in the network is ____.

7. (NN) 
Given a $[5,6,6,3]$ neural network (5 input neurons, 6 neurons in hidden layer 1, 6 neurons in hidden layer 2, 3 output neurons), the number of multiplication operations required for the forward pass (predicting output from the input) is ____.

8. (NN) There is an error in the following code
```python showLineNumbers
1. x_train,x_test,y_train,y_test = train_test_split(x,yd,test_size=0.1, random_state=42) 
2. model = tf.keras.Sequential()
3. model.add(tf.keras.layers.Dense(20,input_shape=(1,), activation='relu'))
4. model.add(tf.keras.layers.Dense(20, activation='relu'))
5. model.add(tf.keras.layers.Dense(1))
6. model.compile(optimizer='sgd',loss='categorical_crossentropy')
7. model.fit(x_train, y_train, validation_split=0.1, batch_size = 32, epochs = 20, verbose = 1)
```
Which of the following changes will surely resolve the error?
  - 6. model.compile(optimizer='sgd',loss='mse')
  - 5. model.add(tf.keras.layers.Dense(5))
  - 7. model.fit(x_train, y_train, validation_split=0.1, batch_size = 32, epochs = 20, verbose = 3)
  - 5. model.add(tf.keras.layers.Dense(1, activation=sigmoid))
  - None of these

9. (NN) A non-linear model $\hat{y} = \sigma(w_0 + w_1x)$
 is to be optimized using the gradient descent algorithm over the loss term $\mathit{L} = (y - \hat{y})^2$
. Here, $\sigma(\cdot)$
 is the sigmoid function. The weights are chosen to be $w_0 = \log_e(2)$ and $w_1=\log_e(0.5)$. The learning rate $\eta = 1$. Find the updated value of $w_0$ after iterating once over the training data $(x = 2, y = 2/3)$.

10. (NN) For multi-label classification, a neural network has 3 inputs. There is no hidden layer. The output layer has 2 neurons.
  - What should be the non-linearity in the output layer?
  - What loss function should be used to train the network?
  - Derive the update rule for all the weights.

11. (NN) In rose-lotus classification problem, a single-layer neural network is used with weights $W=\left[\begin{array}{cc}-0.5&2\\-1&2\end{array} \right]$. The output $\hat{\bm{y}}=W\bm{x}$ corresponds to rose and lotus, respectively. The size of a rose is $\bm{x}=\left[\begin{array}{c}5\\2\end{array} \right]$, respectively. 
  - If we formulate the problem as multi-class classification (2-classes), find the loss value for this flower.
  - If we formulate the problem as multi-label classification (label as rose or not-rose), find the loss value for this flower.

12. (NN) (10 marks) A gardener supplies >10,000 flowers daily which contain hundreds of roses mixed with other flowers. A camera takes the image of each flower (one flower at a time). You are asked to choose 100 roses (only roses, no other flower) and deliver them to a florist. Design an ML system that can help you. Write the complete process step by step (from data preparation to deployment).
Explain all the steps using concepts studied in the course.
