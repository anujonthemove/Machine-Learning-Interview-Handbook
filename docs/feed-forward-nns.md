
#### Q. What are Feed Forward Neural Networks?
    
Typically, the computation in a Feed Forward Neural Network is organized in a Directed Acyclic Computational Graph(DAG) in the following manner:

- **Forward Pass**

    Input data → feature extractor (linear transform + **activation** function) → output/prediction(**classification**/**regression**) → loss calculation (using **loss function**)
    
    - A neural network in the forward pass makes a guess with it's initial values of parameters, it then checks how correct it was to the ground truth labels provided in the dataset using the cost function. Based on the loss, it then makes the backward pass.

- **Backward Pass**
    
    **Backpropagation of error algorithm** (calculation of gradients using chain rule from last layer to first layer) → **Gradient Descent** **Optimization algorithm**(updates the weights/parameters of the model in order to minimize the loss function)
    
    - Compute the gradients or derivatives of the loss function with respect to the model weights/parameters
        - In simple words, derivative of a (cost say J(w, b))function with respect to it's parameters (say w, b) means we are interested in knowing what will happen to the function when we change the values of it's parameters.
    - Using the computed gradients, adjust these weights/parameters
    - … do a forward pass again and find out how the cost function changed on changing the values of weights/parameters …
    - We need to check the derivative of the cost function with respect to each of the parameters. For a simple computation graph given by $J = 3(a+bc)$, we need to find out how does J change when we change each of a, b, and c
- is trained using the gradient descent optimization algorithm and the backpropagation of error algorithm.
    - **GD updates the parameters of a predictive model to minimize a loss function. It does that by using the gradients of the loss function with respect to the parameters.**
    - **BP provides one way to calculate those gradients.**

    Ref: [https://stackoverflow.com/questions/36740533/what-are-forward-and-backward-passes-in-neural-networks](https://stackoverflow.com/questions/36740533/what-are-forward-and-backward-passes-in-neural-networks)
    
#### Q. What is the use of Bias term?
The bias term provides more flexibility to a model while learning the weights in a solution space. The model becomes more flexible to adapt to the optimal/best values.

[https://www.turing.com/kb/necessity-of-bias-in-neural-networks](https://www.turing.com/kb/necessity-of-bias-in-neural-networks)

[https://towardsdatascience.com/why-we-need-bias-in-neural-networks-db8f7e07cb98](https://towardsdatascience.com/why-we-need-bias-in-neural-networks-db8f7e07cb98)

#### Q. Are neural networks convex?

Neural netowrks are not essentially convex, since they are differentiable, they can be decomposed into a number of convex problems    

[https://stats.stackexchange.com/questions/106334/cost-function-of-neural-network-is-non-convex](https://stats.stackexchange.com/questions/106334/cost-function-of-neural-network-is-non-convex)

[https://medium.com/lsc-psd/convex-optimization-in-deep-learning-ea90f1ed1c5d](https://medium.com/lsc-psd/convex-optimization-in-deep-learning-ea90f1ed1c5d)

- From CS231n:

    Functions like the SVM Loss function is an example of a Convex Function. There is a large amount of literature devoted to efficiently minimizing these types of functions, Once we extend our score functions ff to Neural Networks our objective functions will become non-convex.

#### Q. What are logits?

Logits interpreted to be the unnormalised (or not-yet normalised) predictions (or outputs) of a model. These can give results, but we don't normally stop with logits, because interpreting their raw values is not easy

https://datascience.stackexchange.com/questions/31041/what-does-logits-in-machine-learning-mean

For example, in case of a multi-class classification problem, logits refer to a vector of raw prediction values for each category. These logits are not scaled to add up to 1 so they are normally fed into a softmax to turn them into prob for each category.


