??? question  "Explain Gradient Descent Algorithm"
    Check Feed Forward Neural Networks section for explanation

??? question  "Do we need to use a learning rate scheduler for adaptive optimizers like Adam, AdaGrad?"
    
    We use use Learning Rate Scheduler with SGD but the same may not be required for Adaptive optimizers like Adam.

    Adam manages learning rates internally, it's incompatible with most learning rate schedulers.

    Adaptive optimizers eschew the use of a separate learning rate scheduler, choosing instead to embed learning rate optimization directly into the optimizer itself.

    It was discovered relatively early on that choosing a large initial learning rate then shrinking it over time leads to better converged, more performant models. ***This is known as annealing or decay***.

    SGD + LR Scheduler works better than SGD + Fixed LR

    Some common LR Schedulers:

    - ReduceLROnPlateau → SGD+ReduceLROnPlateau+EarlyStopping
    - Cosine annealed warm restart
    - One-cycle learning rate schedulers - **superconvergence**

    Found an answer on Stackexchange which warrants a discussion:

    [https://stats.stackexchange.com/questions/286723/is-manually-tuning-learning-rate-during-training-redundant-with-optimization-met](https://stats.stackexchange.com/questions/286723/is-manually-tuning-learning-rate-during-training-redundant-with-optimization-met)

    [https://spell.ml/blog/lr-schedulers-and-adaptive-optimizers-YHmwMhAAACYADm6F](https://spell.ml/blog/lr-schedulers-and-adaptive-optimizers-YHmwMhAAACYADm6F)
        
??? question  "Difference between backprop and gradient descent?"
    Backpropagation is a process of calulating derivatives (using the chain rule in a feed forward neural network, the gradient calulcation flows from the last layer to the first layer)

    Gradient descent is an optimizer which is used to adjust the values of parameters

??? question  "Is gradient descent first order or second order optimizer?"
    
    It is the first order optimizer
    
??? question  "What are some second-order methods? Are they used in optimization?"
    
    We will not discuss algorithms that are infeasible to compute in practice for high-dimensional data sets, e.g. second-order methods such as Newton's method.
    
??? question  "Explain Adam optimizer"
    - Adaptive Moment Estimation (Adam) is another method that computes adaptive learning rates for each parameter.

    - In addition to storing an exponentially decaying average of past squared gradients vt like Adadelta and RMSprop, Adam also keeps an exponentially decaying average of past gradients mt similar to momentum.

    - Adam is almost parameter-free. Adam does have a learning rate hyperparameter, but the adaptive nature of the algorithm makes it quite robust—unless the default learning rate is off by an order of magnitude, changing it doesn't affect performance much.

??? question  "What is Synchronous SGD?"