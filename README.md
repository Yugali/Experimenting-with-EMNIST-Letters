# Expermenting-with-EMNIST-Letters
Libraries
You will need Keras and TensorFlow. While other backends will work, the Keras documentation recommends TensorFlow, and we will want to use the TensorBoard visualization tools.
The TensorFlow documentation steers you toward TensorFlow 2 and tf.keras, but if you are installing and running TensorFlow locally, you may have have an easier time with the latest stable version. Note that you will need to install a different Python package to enable GPU support.
You may also find a use for scikit-learn and Pandas.

Warm-Up
Keras includes several datasets and examples, many using MNIST. In particular, take a look at mnist_mlp.py and mnist_cnn.py, and compare them to the networks developed in Chapter 6 of the textbook.
Try running mnist_cnn.py and verify that you can match the accuracy of 99.25% claimed in the comments.
Nielsen claims an accuracy of 99.60%.(see Inserting an extra fully-connected layer). Modify mnist_cnn.py to match the parameters of that model, and compare your results.

Training on EMNIST Letters
Apply the same convolutional network architecture to the EMNIST Letters dataset. How does the accuracy compare to MNIST? How does the accuracy compare to the MLP you trained in Project 2?
Visualizing Training Progress
Recall that the fit() method on a Keras Model returns a History object. You can use this to visualize a training history, if the training process doesn’t take too long.
When training is slow (as it will be for deep networks, even with a GPU), you might like to receive some additional feedback on the process. The fit() method’s optional verbose argument provides some information, but TensorFlow includes the TensorBoard suite of tools for better visualizing metrics.
Keras includes a TensorBoard callback that can write metrics to be read by the tensorboard command-line tool. See this article for a simple example.
If you are running your model in the cloud, the path of least resistance is to use TensorFlow 2’s %tensorboard magic. Otherwise you will need to jump through some extra hoops.

Experimenting with EMNIST Letters
Now that you have a baseline convolutional network for comparison, begin experimenting with alternate architectures and optimizations for the EMNIST Letters dataset. Can you reach an accuracy of 90% or above?

Tips
Don’t forget to use a validation set to avoid overfitting. The Keras examples aren’t always careful about this.
Try viewing some of the misclassified letters with matplotlib.pyplot.imshow().
Recall that EMNIST Letters merges upper- and lowercase letters into the same class. How might you design a network that accounts for that difference?
When finished, evaluate your results on the test set. Compare the performance on the test set with your previous networks.

