??? question "Why do we use Convolutional Neural Networks(CNNs) for images/videos? What are the advantages of using CNNs over vanilla Neural Networks?"
    1. Spatial arrangement: Information in an image makes more sense spatially. CNNs preserve spatial structure in images.

    2. Local Connectivity: CNNs take advantage of **Local Spatial Coherence** in the input. As opposed to vanilla Neural Networks where every neuron is connected to all neuron in the previous volume, in CNNs each neuron is connected to only a local region of the input volume. This local region exposed to a neuron in the input volume is called **Local Receptive Field**. Receptive field of a single unit within a layer is determined by the size of filter(width, height).

    3. Weight/Parameter Sharing: The weights of a kernel or filter used in a layer are learnable. This filter convolves with the input volume to produce an output feature map. The weights of a particular filter is shared across the input which produces this output. Due to this, a feature (say an edge, corner) learned at one spatial location doesn't need to be learned again if the same is found at another spatial location in the input.


    Read more:
    
    * https://cs231n.github.io/convolutional-networks/

    * https://towardsdatascience.com/understand-local-receptive-fields-in-convolutional-neural-networks-f26d700be16c

    * https://towardsdatascience.com/understanding-parameter-sharing-or-weights-replication-within-convolutional-neural-networks-cc26db7b645a

    * https://www.quora.com/What-are-the-advantages-of-a-convolutional-neural-network-CNN-compared-to-a-simple-neural-network-from-the-theoretical-and-practical-perspective

    * https://msail.github.io/post/cnn_human_visual/


??? question "What are Receptive Fields in CNNs?"

    [https://distill.pub/2019/computing-receptive-fields/#overview](https://distill.pub/2019/computing-receptive-fields/#overview)

    [https://blog.christianperone.com/2017/11/the-effective-receptive-field-on-cnns/](https://blog.christianperone.com/2017/11/the-effective-receptive-field-on-cnns/)

    [https://theaisummer.com/receptive-field/](https://theaisummer.com/receptive-field/)