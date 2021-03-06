# Handwriting Classifier - Machine Learning Recipes #7

[![Known Vulnerabilities](http://snyk.io/test/github/mramshaw/Intro-to-ML/badge.svg?style=plastic&targetFile=Handwriting_Classifier%2Frequirements.txt)](http://snyk.io/test/github/mramshaw/Intro-to-ML?style=plastic&targetFile=Handwriting_Classifier%2Frequirements.txt)

![Final_Graphic](images/Figure_6.png)

There are a wide variety of installation options for [TensorFlow](https://www.tensorflow.org/install/).

While the video deals with the [Docker](https://hub.docker.com/r/tensorflow/tensorflow/) option, this exercise uses the `pip` option - updated for __TensorFlow 1.5.0__.

Note that, for GPU-based TensorFlow, there is also an [nvidia-docker](https://github.com/NVIDIA/nvidia-docker) option.

There is a very useful [Jupyter notebook](https://github.com/random-forests/tutorials/blob/master/ep7.ipynb), which is definitely worth a look.

For more information, refer to the [TensorFlow layers](https://www.tensorflow.org/tutorials/layers) tutorial.

## MNIST Data

Like `sklearn` with its `load_iris()` convenience method, `TensorFlow` also has convenience methods
for the [MNIST dataset](http://yann.lecun.com/exdb/mnist/).

Run the following Python code to download it:

    import tensorflow as tf
    tf.logging.set_verbosity(tf.logging.ERROR)

    learn = tf.contrib.learn

    mnist = learn.datasets.load_dataset('mnist')

The results should look as follows:

    Successfully downloaded train-images-idx3-ubyte.gz 9912422 bytes.
    Extracting MNIST-data/train-images-idx3-ubyte.gz
    Successfully downloaded train-labels-idx1-ubyte.gz 28881 bytes.
    Extracting MNIST-data/train-labels-idx1-ubyte.gz
    Successfully downloaded t10k-images-idx3-ubyte.gz 1648877 bytes.
    Extracting MNIST-data/t10k-images-idx3-ubyte.gz
    Successfully downloaded t10k-labels-idx1-ubyte.gz 4542 bytes.
    Extracting MNIST-data/t10k-labels-idx1-ubyte.gz
    $

Now the MNIST data will be available for subsequent runs.

## Execution

Run the Python code as follows:

    $ python handwriting_classifier.py 

The results should look as follows:

    Extracting MNIST-data/train-images-idx3-ubyte.gz
    Extracting MNIST-data/train-labels-idx1-ubyte.gz
    Extracting MNIST-data/t10k-images-idx3-ubyte.gz
    Extracting MNIST-data/t10k-labels-idx1-ubyte.gz
    Features of each image (28x28) = 784
    Accuracy = 0.921599984169
    $

Note that the accuracy slightly exceeds the 0.9141 we were looking for.

Of course, to get more accurate results there is [Deep MNIST](https://www.tensorflow.org/versions/r1.0/get_started/mnist/pros) - which is supposed to give 99% accuracy.

#### Visualization

The visualized graphics were as follows:

![Figure_1](images/Figure_1.png)

![Figure_2](images/Figure_2.png)

![Figure_3](images/Figure_3.png)

#### Predicted

The prediction results were as follows:

![Correctly_Predicted](images/Figure_4.png)

![Incorrectly_Predicted](images/Figure_5.png)

#### Final Results

For a nice explanation of the final visualization, watch the following [link](https://youtu.be/Gj0iyo265bc?list=PLOU2XLYxmsIIuiBfYad6rFYQU_jL2ryal&t=340).

## Credits

    https://www.youtube.com/watch?v=Gj0iyo265bc
