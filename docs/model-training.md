#### Q. What is iteration, epoch, batch size, step size?

* A Forward Backward and forward pass makes together one **iteration.**

* During one iteration we can either pass a subset of dataset or **“mini-batch”**or the entire dataset **“batch”.**

* One full pass through the entire dataset(full batch or in mini-batches) is known as an **epoch.** One epoch contains (number_of_items / batch_size) iterations.

* Step size

[https://stackoverflow.com/questions/36740533/what-are-forward-and-backward-passes-in-neural-networks](https://stackoverflow.com/questions/36740533/what-are-forward-and-backward-passes-in-neural-networks)

[https://spell.ml/blog/lr-schedulers-and-adaptive-optimizers-YHmwMhAAACYADm6F](https://spell.ml/blog/lr-schedulers-and-adaptive-optimizers-YHmwMhAAACYADm6F)


#### Q. What is the effect of varying batch size on asymptotic test accuracy?
<!-- 1. A higher batch sizes could lead to lower asymptotic test accuracy. We can recover the lost test accuracy from a larger batch size by increasing the learning rate - take this conclusion with a grain of salt. It is known that simply increasing the learning rate does not fully compensate for large batch sizes in more complex datasets (than MNIST)
    
Starting with a large batch size doesn’t “get the model stuck” in some neighbourhood of bad local optimums. The model can switch to a lower batch size or higher learning rate anytime to achieve better test accuracy.

Batch size decides how soon your model updates it's weights. If batch size = 1 then the model makes weight updates everytime it sees an example. This would lead to a noisy weight update. Batching the data introduces noisyness in the data hence batch size becomes an important parameter that needs to be taken care of -->

#### Q. Why using mini-batch gradient descent is a good choice? - * From ruder.io:
<!-- 1. Reduces the variance of the parameter updates, which can lead to more stable convergence; and

2. Doing so can make use of highly optimized matrix optimizations common to state-of-the-art deep learning libraries that make computing the gradient w.r.t. a mini-batch very efficient.


[https://medium.com/mini-distill/effect-of-batch-size-on-training-dynamics-21c14f7a716e](https://medium.com/mini-distill/effect-of-batch-size-on-training-dynamics-21c14f7a716e)

[https://androidkt.com/batch-size-step-iteration-epoch-neural-network/](https://androidkt.com/batch-size-step-iteration-epoch-neural-network/) -->
    

#### Q. What does a large gap between training and validation graph signifies?

If there’s a big gap between the training and the validation curves, clearly the model strongly overfits. 

#### Q. Reasons we get NaN in loss values when training a neural network

<!-- when the number of input classes do not match the shape of the final classification layer in the model -->

#### Q. How do you decide the learning rate for training a model?
<!-- - for ConvNets, we usually choose learning rate using log scale, refer this for more depth: [https://cs231n.github.io/neural-networks-3/#anneal](https://cs231n.github.io/neural-networks-3/#anneal)

[https://www.jeremyjordan.me/nn-learning-rate/](https://www.jeremyjordan.me/nn-learning-rate/)

[https://towardsdatascience.com/estimating-optimal-learning-rate-for-a-deep-neural-network-ce32f2556ce0](https://towardsdatascience.com/estimating-optimal-learning-rate-for-a-deep-neural-network-ce32f2556ce0)
    
The training should start from a relatively large learning rate because, in the beginning, random weights are far from optimal, and then the learning rate can decrease during training to allow more fine-grained weight updates. - VERY CONFLICTING with below thread 

[https://stats.stackexchange.com/questions/499013/adam-adaptive-optimizers-learning-rate-tuning?rq=1](https://stats.stackexchange.com/questions/499013/adam-adaptive-optimizers-learning-rate-tuning?rq=1) -->


#### Q. How to speed up your learning? 
**(From Coursera Deep Learning Sp)**

Use Learning rate decay!

The idea is as you move towards convergence, using a fixed learning rate, you might wander around the optima but may not reach it so reducing the LR can help converge.

During the initial phase, when LR is large, you can still have relatively fast learning, meaning that during initial steps of learning you can afford to take larger steps but as and when you approach convergence, then having a lower learning rate can allow you to take smaller steps

Decay Rate is a HYPERPARAMETER that one needs to choose just like the learning rate.

#### Q. Vanishing or Exploding Gradients
* can be improved by careful weight initialization - partial solution