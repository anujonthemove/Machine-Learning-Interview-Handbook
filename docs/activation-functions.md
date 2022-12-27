### Generic

#### Q. What are activation functions? 
#### Q. What is the use of activation functions in Deep Learning? 
#### Q. What are some of the commonly used activation functions?

* [https://www.v7labs.com/blog/neural-networks-activation-functions](https://www.v7labs.com/blog/neural-networks-activation-functions)

* [https://medium.com/analytics-vidhya/activation-functions-all-you-need-to-know-355a850d025e](https://medium.com/analytics-vidhya/activation-functions-all-you-need-to-know-355a850d025e)

* [https://towardsdatascience.com/what-is-activation-function-1464a629cdca](https://towardsdatascience.com/what-is-activation-function-1464a629cdca)

* [https://towardsdatascience.com/7-popular-activation-functions-you-should-know-in-deep-learning-and-how-to-use-them-with-keras-and-27b4d838dfe6](https://towardsdatascience.com/7-popular-activation-functions-you-should-know-in-deep-learning-and-how-to-use-them-with-keras-and-27b4d838dfe6)

* [https://www.superannotate.com/blog/activation-functions-in-neural-networks](https://www.superannotate.com/blog/activation-functions-in-neural-networks)


* Paper: [https://arxiv.org/pdf/2101.09957v1.pdf](https://arxiv.org/pdf/2101.09957v1.pdf)

#### Q. Why do we need non-linear activation functions in Neural Networks?
* [https://stackoverflow.com/questions/9782071/why-must-a-nonlinear-activation-function-be-used-in-a-backpropagation-neural-net](https://stackoverflow.com/questions/9782071/why-must-a-nonlinear-activation-function-be-used-in-a-backpropagation-neural-net)


___


### Specific

#### Q. Why should we avoid using Sigmoid activation in hidden layers?

1. Saturating function - kills neurons with very large or very small input values.

2. It’s output is not zero-centered. Zero-centered data prevents zig zig updates to weights.
    Remember: bowl shape vs circular shape regime for updates.

3. Exponential functions are a bit expensive to compute hence it can slow down the network

#### Q. Why does Tanh activation function works better than sigmoid for hidden units?

It usually works better than sigmoid activation function for hidden units because range of output lies between -1 to 1 therefore it solves the problem of zero-centering the data hence the mean of its output is closer to zero, and so it centers the data better for the next layer.
     
#### Q. Can ReLUs be used for universal approximation?
Yes, they can do so when they are in abundance.

* [https://towardsdatascience.com/if-rectified-linear-units-are-linear-how-do-they-add-nonlinearity-40247d3e4792](https://towardsdatascience.com/if-rectified-linear-units-are-linear-how-do-they-add-nonlinearity-40247d3e4792)

#### Q. Why or how is ReLU non-linear?
*   [https://ai.stackexchange.com/questions/6468/why-do-we-prefer-relu-over-linear-activation-functions](https://ai.stackexchange.com/questions/6468/why-do-we-prefer-relu-over-linear-activation-functions)
    
*   [https://ai.stackexchange.com/questions/5493/what-is-the-purpose-of-an-activation-function-in-neural-networks/5521#5521](https://ai.stackexchange.com/questions/5493/what-is-the-purpose-of-an-activation-function-in-neural-networks/5521#5521)
    
*   [https://ai.stackexchange.com/questions/5601/how-exactly-can-relus-approximate-non-linear-and-curved-functions](https://ai.stackexchange.com/questions/5601/how-exactly-can-relus-approximate-non-linear-and-curved-functions)
    
*   [https://medium.com/@maximlopin/why-is-relu-non-linear-aa46d2bad518](https://medium.com/@maximlopin/why-is-relu-non-linear-aa46d2bad518)


#### Q. Why do we use ReLUs when they are not differentiable?
We do not use gradients, we use sub-gradients for the parts other than x=0

*   [https://www.quora.com/Why-does-ReLU-work-with-backprops-if-its-non-differentiable](https://www.quora.com/Why-does-ReLU-work-with-backprops-if-its-non-differentiable)


#### Q. What are some of the advantages and disadvantages of using ReLU?

**Advantages:**

1. Linearity: 
    1. ReLU has a linear component for positive values. Linear activation functions are easier to optimize and allow for a smooth flow so, it is best suited for supervised tasks on large sets of labelled data. 
    2. Networks using ReLU converge faster than that with Sigmoid and Tanh as there is no exponential function involved, just the max operation.
    3. This also avoids killing of gradients of large and small positive values
2. Computation: It is computationally cheaper than Sigmoid and tanh. Also, the derivative remains constant for a positvie input. This reduces time taken during model learning.
3. Differentiable
4. Representational Sparsity: It is capable of outputting a true zero value.


**Disdvantages:**

1. It’s output is not zero-centered
2. Does not deal with negative values in a meaningful way
3. RNNs, LSTMs cannot use ReLUs due to their Logic gate structure
4. **Exploding Gradient:** This occurs when the gradient gets accumulated. It causes a large differences in the subsequent weight updates, as a result it causes instability during model convergence.
5. **Dying ReLU:** The problem of "dead neurons" occurs when the neuron gets stuck in the negative side and constantly outputs zero. In case of ReLU, because gradient of 0 is also 0, it's unlikely for the neuron to ever recover. **This happens when the learning rate is too high or negative bias is quite large.**

[https://iq.opengenus.org/relu-activation/](https://iq.opengenus.org/relu-activation/)


[https://www.kaggle.com/code/dansbecker/rectified-linear-units-relu-in-deep-learning/notebook](https://www.kaggle.com/code/dansbecker/rectified-linear-units-relu-in-deep-learning/notebook)

