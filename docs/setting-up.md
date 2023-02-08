??? question "Why is it important to have a zero-centered data?"

    - It is important to have zero-centered data for input to Neural Networks because it helps to ensure that the input features are on a similar scale, which can improve the performance of the network. When the features of the input data are on different scales, some features may dominate others, making it difficult for the network to learn meaningful representations of the data. By zero-centering the data, the mean of the input features is subtracted from each feature, so that the mean of the input data is 0.  
    
    - Additionally, zero-centering the data can help to speed up convergence of the optimization algorithm, as it helps to ensure that the optimization problem is well-conditioned.


??? question "What is feature scaling?"
    - Feature scaling is a pre-processing step in deep learning where the values of the input features are normalized to a common range. 
    
    - The goal of feature scaling is to avoid having input features with large magnitude dominate the learning process of the model. 
    
    - Common scaling techniques include standardization, where features are transformed to have zero mean and unit variance, and normalization, where features are rescaled to a specific range such as [0, 1].

??? question "What is the difference between Standardization and Normalization?"

    - Standardization and normalization are two techniques used to preprocess input data in deep learning.
    
    - Standardization involves transforming the data so that it has a mean of 0 and a standard deviation of 1. This means that the data is centered around the origin and scaled so that it has similar magnitudes. This is often used when the features in the input data have different scales and units, as it allows the model to treat all features equally.
    
    - Normalization, on the other hand, involves transforming the data so that it has a minimum of 0 and a maximum of 1. This is often used when the input data is sparse and has a wide range of values. Normalization ensures that the scale of the data does not have an impact on the performance of the model.
    
    - In summary, standardization is used to center and scale the data, while normalization is used to rescale the data so that it has a minimum and maximum value.