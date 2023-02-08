??? question "What are activation functions? Why do we need non-linear activation functions in Neural Networks?"

    - Activation functions are mathematical operations applied to the output of each neuron in a neural network. They introduce non-linearity into the output, allowing the network to learn complex relationships between inputs and outputs. Common activation functions include sigmoid, tanh, ReLU (rectified linear unit), and softmax.

??? question "What are some of the most commonly used activation functions?"
    - Read more:

        - [https://www.v7labs.com/blog/neural-networks-activation-functions](https://www.v7labs.com/blog/neural-networks-activation-functions) 

        - [https://medium.com/analytics-vidhya/activation-functions-all-you-need-to-know-355a850d025e](https://medium.com/analytics-vidhya/activation-functions-all-you-need-to-know-355a850d025e)

        - [https://towardsdatascience.com/what-is-activation-function-1464a629cdca](https://towardsdatascience.com/what-is-activation-function-1464a629cdca)

        - [https://arxiv.org/pdf/2101.09957v1.pdf](https://arxiv.org/pdf/2101.09957v1.pdf)


??? question "Why should we avoid using Sigmoid activation in hidden layers?"
    
    1. It is a saturating function. It kills neurons with very large or very small input values.
    2. It’s output is not zero-centered. Zero-centered data prevents zig zig updates to weights.
    3. Exponential functions are a bit expensive to compute hence it can slow down the network

??? question "Why does Tanh activation function works better than sigmoid for hidden units?"

    - It usually works better than sigmoid activation function for hidden units because range of output lies between -1 to 1 therefore it solves the problem of zero-centering the data hence the mean of its output is closer to zero, and so it centers the data better for the next layer.
     
??? question "Can ReLUs be used for universal approximation?"
    - Yes, ReLU (rectified linear unit) activation functions can be used for universal approximation. 
    - Universal approximation refers to the property that a neural network with a single hidden layer containing a sufficient number of neurons can approximate any continuous function to any desired accuracy. This means that with enough neurons and appropriate training, a neural network with ReLU activation functions can model a wide range of complex, non-linear functions. However, in practice, it is typically necessary to use multiple hidden layers in order to achieve good performance on more difficult problems.

    - Read more:
        - [If Rectified Linear Units Are Linear, How Do They Add Nonlinearity?](https://towardsdatascience.com/if-rectified-linear-units-are-linear-how-do-they-add-nonlinearity-40247d3e4792)

??? question "Why or how is ReLU non-linear?"

    - The ReLU activation function is considered non-linear because it introduces non-linearity into the output of a neuron. The ReLU function takes the input value x and returns x if x is positive, and 0 if x is negative. This results in a step-like function, which is not a linear function, and is thus considered non-linear.
    
    - Linear functions have the property that the output is proportional to the input, and the relationship between the input and output can be described by a single line. On the other hand, non-linear functions have more complex relationships between inputs and outputs, and cannot be described by a single line.
    
    - By introducing non-linearity through the use of ReLU activation functions, neural networks are able to model more complex relationships between inputs and outputs, which is important for solving many real-world problems.

??? question "Why do we use ReLUs when they are not differentiable?"

    - ReLU activation functions are not differentiable at x=0, but this is not a significant issue in practice because gradient-based optimization algorithms only need to be able to compute the gradient of the loss function with respect to the network parameters, not the activation function itself. The gradient of the ReLU function is simply 0 for x<0, and 1 for x>0, which can be easily calculated and used in optimization algorithms like stochastic gradient descent.

    - ReLU activation functions have several advantages over other activation functions that make them popular for use in neural networks. They are computationally efficient, as they only require a simple comparison operation to calculate. They also introduce sparsity into the activations of the network, as many of the neurons will produce 0 output, making the network more interpretable and reducing the risk of overfitting. Additionally, they have been found to result in faster convergence and better performance on many problems compared to other activation functions.

    - In conclusion, the lack of differentiability of ReLU at x=0 is not a significant issue in practice, and the benefits of using ReLU activation functions outweigh this limitation.


??? question "What are some of the advantages and disadvantages of using ReLU?"

    **Advantages:**

    1. Computationally Efficient: ReLU activation functions are simple and fast to compute, requiring only a simple comparison operation.
        
    2. Introduces Sparsity: ReLU activation functions introduce sparsity into the activations of the network, as many neurons will produce 0 output, making the network more interpretable and reducing the risk of overfitting.
    
    3. Improves Convergence: ReLU activation functions have been found to result in faster convergence and better performance on many problems compared to other activation functions.
    
    4. Non-saturating: ReLU activation functions do not saturate, meaning that they do not become asymptotic, which can improve the speed of convergence in some cases.
    
    5. Can be Used in Deep Networks: ReLU activation functions are often used in deep networks as they help to overcome the vanishing gradient problem, where the gradients become very small, making it difficult for the network to learn.

    **Disdvantages:**

    1. Dying ReLU Problem: ReLU activation functions can suffer from the "dying ReLU" problem, where a large number of neurons become inactive, producing 0 output, making it difficult for the network to learn.
    
    2. Sensitive to Noise: ReLU activation functions can be sensitive to noisy inputs, as a small change in the input can result in a large change in the output.
    
    3. Can cause Exploding Gradients: ReLU activation functions can sometimes cause exploding gradients, where the gradients become very large, making it difficult for the optimization algorithms to learn.
    
    4. May Require Careful Initialization: The weights of a network with ReLU activation functions may need to be initialized carefully in order to prevent the "dying ReLU" problem and to ensure that the network can learn effectively.

    Read more:

    - [https://iq.opengenus.org/relu-activation/](https://iq.opengenus.org/relu-activation/)
    
    - [https://www.kaggle.com/code/dansbecker/rectified-linear-units-relu-in-deep-learning/notebook](https://www.kaggle.com/code/dansbecker/rectified-linear-units-relu-in-deep-learning/notebook)