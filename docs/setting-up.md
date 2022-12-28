#### Q. Why it is important to have a zero-centered data?
<!-- - [https://stats.stackexchange.com/questions/237169/why-are-non-zero-centered-activation-functions-a-problem-in-backpropagation](https://stats.stackexchange.com/questions/237169/why-are-non-zero-centered-activation-functions-a-problem-in-backpropagation)
- [https://ai.stackexchange.com/questions/26958/why-is-it-a-problem-if-the-outputs-of-an-activation-function-are-not-zero-center](https://ai.stackexchange.com/questions/26958/why-is-it-a-problem-if-the-outputs-of-an-activation-function-are-not-zero-center)
- [https://arxiv.org/pdf/2004.06632.pdf#:~:text=The sigmoid function is bound,of (0%2C1)](https://arxiv.org/pdf/2004.06632.pdf#:~:text=The%20sigmoid%20function%20is%20bound,of%20(0%2C1)).
- Very very important: [https://rohanvarma.me/inputnormalization/](https://rohanvarma.me/inputnormalization/) - effect of zero centring the data especially when using sigmoid -->

#### Q. Feature Scaling: Standardization vs Normalization
[https://towardsdatascience.com/normalization-vs-standardization-quantitative-analysis-a91e8a79cebf](https://towardsdatascience.com/normalization-vs-standardization-quantitative-analysis-a91e8a79cebf)

- Both are feature scaling methods
- Every dataset does not require features scaling.
- It is required only when features have different ranges.
- 2 techniques:
    - Normalization(also called min-max scaling): features will be rescaled so that the data will fall in the range of [0,1]
    - Standardization (also called, Z-score normalization): the features will be rescaled so that they’ll have the properties of a standard normal distribution with mean,μ=0 and standard deviation, σ=1; where μ is the mean (average) and σ is the standard deviation from the mean. This scales the features in a way that they range between [-1,1]
- [https://stats.stackexchange.com/questions/10289/whats-the-difference-between-normalization-and-standardization](https://stats.stackexchange.com/questions/10289/whats-the-difference-between-normalization-and-standardization)
- **Implications**: if you have outliers in your feature (column), normalizing your data will scale most of the data to a small interval, which means all features will have the same scale but does not handle outliers well. Standardisation is more robust to outliers, and in many cases, it is preferable over Max-Min Normalisation. [https://www.kdnuggets.com/2020/04/data-transformation-standardization-normalization.html](https://www.kdnuggets.com/2020/04/data-transformation-standardization-normalization.html)


#### Q. What is Batchnorm?