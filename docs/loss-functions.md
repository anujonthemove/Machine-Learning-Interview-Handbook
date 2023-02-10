??? question "What is a cost function?"

    * In deep learning, a cost function, also known as a loss function, is a mathematical function that measures the difference between the predicted output of a model and the actual target output. The goal of training a deep learning model is to minimize the value of the cost function, so that the model's predictions are as close as possible to the target outputs.

    * The cost function is used to guide the optimization process during training by providing a measure of the error in the model's predictions. The optimization algorithm, such as stochastic gradient descent (SGD), updates the model's weights and biases in the direction that reduces the value of the cost function.

    * There are many different cost functions that can be used in deep learning, depending on the type of problem being solved and the type of model being used. Common examples include mean squared error for regression problems, cross-entropy for binary classification problems, and categorical cross-entropy for multi-class classification problems.


??? question "Cost vs Loss function?"

    * Loss function is defined on a single training example.
    * Cost function is defined on the entire training set.


??? question "What are some Regression Loss Functions?"

    1. Mean Absolute Error/L1
    2. Mean Squared Error/L2 
    3. Root Mean Squared Error
    4. Mean Bias Error
    5. Huber Loss
    6. Mean Squared Logarithmic Error Loss
    7. Mean Absolute Error Loss
    
    Choosing the right loss function for a regression problem depends on the specific requirements of the problem and the type of data being used. In general, MSE and MAE are a good starting point for most regression problems.

    Read more:
        
    * Huber Loss: [https://github.com/christianversloot/machine-learning-articles/blob/main/using-huber-loss-in-keras.md](https://github.com/christianversloot/machine-learning-articles/blob/main/using-huber-loss-in-keras.md)

??? question "What are some Classification Loss Functions?"
    1. Cross-Entropy Loss (Binary/Categorical)
    2. Hinge Loss
    3. Squared Hinge Loss

    Read more:

    * Cross Entropy Loss: [https://gombru.github.io/2018/05/23/cross_entropy_loss/](https://gombru.github.io/2018/05/23/cross_entropy_loss/)
    
    * [https://medium.com/analytics-vidhya/common-loss-functions-in-machine-learning-for-classification-model-931cbf564d42](https://medium.com/analytics-vidhya/common-loss-functions-in-machine-learning-for-classification-model-931cbf564d42)

    * [https://towardsdatascience.com/understanding-loss-functions-the-smart-way-904266e9393](https://towardsdatascience.com/understanding-loss-functions-the-smart-way-904266e9393)


??? question  "What are different types of Multi-Class Classification Loss Functions?"
    1. Binary Cross-Entropy (BCE) 
    2. Categorical Cross-Entropy (CCE):
    3. Hinge Loss
    3. Kullback Leibler Divergence Loss
    4. Focal Loss


??? question  "Probability vs likelyhood"
    Maximum likelihood seeks to find the optimum values for the parameters by maximizing a likelihood function derived from the training data.

    [https://www.youtube.com/watch?v=pYxNSUDSFH4&ab_channel=StatQuestwithJoshStarmer](https://www.youtube.com/watch?v=pYxNSUDSFH4&ab_channel=StatQuestwithJoshStarmer)



??? question  "Why do we use log?"

    [What is logarithm? | Math, Statistics for data science, machine learning](https://www.youtube.com/watch?v=KzQQCtgzQbw&t=3s&ab_channel=codebasics)
    
??? question  "What is information theory, entropy, cross-entropy, KL Divergence?"
    
    **Information Theory:**

    [Very well explained in the beginning of this video](https://www.youtube.com/watch?v=ErfnhcEV1O8&ab_channel=Aur%C3%A9lienG%C3%A9ron)

    **Entropy**:

    It is a measure of how uncertain the events are. It tells you how unpredictable that probability distribution is.
    The formula for entropy is:

    $Entropy = H(p) = -\sum_ip_ilog_2(p_i)$

    It gives us the average amount of information that you get from one sample drawn from a given probability distribution $p$

        
    [https://www.youtube.com/watch?v=YtebGVx-Fxw&ab_channel=StatQuestwithJoshStarmer](https://www.youtube.com/watch?v=YtebGVx-Fxw&ab_channel=StatQuestwithJoshStarmer)

    [https://www.youtube.com/watch?v=IPkRVpXtbdY&ab_channel=mfschulte222](https://www.youtube.com/watch?v=IPkRVpXtbdY&ab_channel=mfschulte222)
        

    **Cross Entropy**

    [https://www.youtube.com/watch?v=tRsSi_sqXjI&ab_channel=Udacity](https://www.youtube.com/watch?v=tRsSi_sqXjI&ab_channel=Udacity)

    [https://www.youtube.com/watch?v=bLb_Kp5Q9cw&ab_channel=MattYedlin](https://www.youtube.com/watch?v=bLb_Kp5Q9cw&ab_channel=MattYedlin)

    [https://www.youtube.com/watch?v=TIL0BU6917o&ab_channel=DrJuanKlopper](https://www.youtube.com/watch?v=TIL0BU6917o&ab_channel=DrJuanKlopper)

    **KL Divergence**

    * The amount by which the cross entropy exceeds the entropy is called the relative entropy or commonly KL Divergence

    * Cross Entropy = Entropy + KL Divergence

        $D_{KL}(p||q) = H(p, q) - H(p)$

    * It is a measure of the information lost when Q is used to approximate P

        [https://stats.stackexchange.com/questions/154879/a-list-of-cost-functions-used-in-neural-networks-alongside-applications](https://stats.stackexchange.com/questions/154879/a-list-of-cost-functions-used-in-neural-networks-alongside-applications)
    
??? question  "How are entropy and probability related?"
    
    [https://www.analyticsvidhya.com/blog/2020/11/entropy-a-key-concept-for-all-data-science-beginners/](https://www.analyticsvidhya.com/blog/2020/11/entropy-a-key-concept-for-all-data-science-beginners/)
    
??? question  "Categorical Cross Entropy Loss vs Sparse Categorical Cross Entropy Loss"
    The main difference is the former one has the output in the form of one-hot encoded vectors whereas the latter has it in integers. 

    The sparse version can also help you when you encounter memory constraint issues are used in multi-class classification. 

    Sparse cross-entropy addresses this by performing the same cross-entropy calculation of error, without requiring that the target variable be one-hot encoded before training.