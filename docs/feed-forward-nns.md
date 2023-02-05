??? question "What are Feed Forward Neural Networks?"
    
    Feed Forward Neural Networks (FFNNs) are organized as a Directed Acyclic Graph (DAG) for computation. FFNNs have two passes: forward pass and backward pass.

    - The forward pass takes input data and passes it through a feature extractor, consisting of a linear transform and an activation function, to produce an output/prediction for either classification or regression. The loss is then calculated using a loss function.

    - The backward pass uses the Backpropagation of error algorithm to calculate the gradients of the loss function with respect to the model parameters using the chain rule from the last layer to the first layer. Then, the Gradient Descent optimization algorithm updates the parameters to minimize the loss function.

    - In summary, a FFNN is trained through the combination of Gradient Descent and Backpropagation.
    

??? question "What is Gradient Descent?"
    
    - Gradient Descent updates the parameters of the model to minimize the loss function by using the gradients of the loss function with respect to the parameters, which can be calculated through Backpropagation.

    
    
??? question "What is the use of Bias term?"

    - The bias term in a neural network is used to shift the activation function to the left or right, allowing the model to fit a more complex decision boundary and improve its accuracy.

    - In other words, it acts as an additional model parameter and allows the model to account for different intercepts or offsets in the input-output mapping.

??? question "Are neural networks convex?"

    - No, in general, neural networks are not convex. 
    - A convex optimization problem has a global minimum that can be found efficiently. However, neural networks can have multiple local minima and it can be challenging to find the global minimum. This is why training neural networks is often **treated** as a non-convex optimization problem and the use of optimization algorithms such as stochastic gradient descent and its variants are used to find good solutions.

    - Neural networks are not essentially convex, since they are differentiable, they can be decomposed into a number of convex problems

??? question "What are logits?"

    - In machine learning, logits refer to the raw, unscaled prediction values that a neural network generates before the activation function is applied. 
    - The logits are typically transformed by an activation function, such as a sigmoid or softmax, to produce a probability distribution over output classes.
    - The logits can be seen as the learned representation of input features by the network and are often used to calculate loss functions during training.