#### Q. What is Regularization?

In the context of deep learning, regularization can be understood as the process of adding information / changing the objective function to prevent overfitting.

It is intended to Lowering the generalization error of a model not the training error.

[Wikipedia](https://en.wikipedia.org/wiki/Regularization_(mathematics))

[https://medium.com/techspace-usict/normalization-techniques-in-deep-neural-networks-9121bf100d8](https://medium.com/techspace-usict/normalization-techniques-in-deep-neural-networks-9121bf100d8)

**Explicit techniques**

* L2 Norm/ L1 Norm - adding panelty to large wt in the cost function -  helps network to have smaller weights and also helps in making the network less sensitive to certain inputs so that makes network predictions less noisy - reduce variance

* Dropout - dropping rand units in the network - introduces noise to network

**Implicit techniques**

* SGD

* Early Stopping - looking at validation set performance

* Getting more data

* Data Augmentation

* Reducing network capacity - Making network more robust

* Gradient Clipping - Helps in exploding gradient problem

* Normalization - more of setting up optimization problem for speeding up training

#### Q. Difference between L1 vs L2 Regularization?
- If you use L1 then the weight matrix w will end up being sparse, w will have a lot of zeros in it and some people say that it can help in compressing the model as some parameters will be zero then you need less memory to store the model

- In practice, L2 is used more in case of NNs

- For NNs, L2 norm is called Frobenius norm of a matrix

- L2 is also sometimes called weight decay


#### Q. What is Dropout?