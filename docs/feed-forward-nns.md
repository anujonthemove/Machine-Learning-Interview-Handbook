
### Theoretical 

#### Q. What are Feed Forward Neural Networks? Describe in detail
    
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

____


### Practical

#### Q. What is iteration, epoch, batch size?
*   A Forward and a Backward pass makes together one **iteration.**

*   During one iteration we can either pass a subset of dataset or **“mini-batch”**or the entire dataset **“batch”.**
*   One full pass through the entire dataset(full batch or in mini-batches) is known as an **epoch.**
    
    [https://stackoverflow.com/questions/36740533/what-are-forward-and-backward-passes-in-neural-networks](https://stackoverflow.com/questions/36740533/what-are-forward-and-backward-passes-in-neural-networks)
