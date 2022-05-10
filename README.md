# Statistical Machine Learning
[Statistical Machine Learning Project](https://colab.research.google.com/drive/11TJvIq79iQNziQAYdtFvk5SgBkrC-r13?usp=chrome_ntp#scrollTo=KqzvGNTTBVE5)

## 1. Background about MNIST

## 2. Data Processing

## 3. Simple Classifiers including KNN, Ada Boosing & SVM with Gaussian Kernel

## 4. Deep Learning Algorithms including the following:

**The project uses Tensorflow and Keras API**.

#### (1). Single layer neural network

Part a: Using sepquential() and for loop to construct the single layer nueral network with more than 5 seeds. I need to create the architecture with 784->100->10, so I add 100 hidden units with ReLU, which does not activate all the neurons at the same time. Then, I add output layer dense(units=10) with softmax, which makes the elements of the output vector are in range (0, 1) and sum to 1. Besides, using SparseCategoricalCrossentropy to compute categorical cross-entropy as the loss, stochastic gradient descent as our optimazer, 20% of the data for validation to complie the model with epoch = 150, batch size = 128.

Part b: It is quite simiar with part (a), except for calculating the misclassification error by using 1 minus the model accuracy.

Part c: In order to visualizing the parameters, the project uses get.weight() to return the weights of current layers, and then plot all the plots using for loop.

Part d: In order to choosing the best value of the parameters, the project does parameter tuning using for loop. The project selects one of the seeds from part(a)(b) to redo part(a) to part(c), to make the lives easiler and save the time.


#### (2). CNN with one 2-D convolutional layer

As the project shows that for single layer neurual network, when epoah = 20, the decreasing of error rate becomes slower, so from now on, it sets epoah = 30. CNN with one 2-D convolutional layer is similary to single layer neural network. It adds con2D and maxplooing for 2D data. And for a convolution with a stride = 1 or for pooling, it should produce output of the same size, so it uses padding = same.

#### (3). CNN with two 2-D convolutional layers

It's almost the same as CNN with one 2-D convolutional layer, except for adding one more layer. In addtion, using dropout(0.5) is a good way to reduces the overfitting.

## 5. More about Deep Learning

#### (1). Data loading and plot examples

#### (2). CNN with one 2-D convolutional layer

It is quite simiar with 4(2), except for the dense units = 19, as it has changed a new dataset, the length of Y_train is 19.

#### (3). CNN with two 2-D convolutional layers

Except for using batch normalization to reduce overfitting, it is the same as 4(3). Since using dropout in training takes a long time, so the projects changes to use batch normalization.

## 5. Reference

Brownlee, J. (2019, July 5). How to visualize filters and feature maps in Convolutional Neural Networks. Machine Learning Mastery. Retrieved May 9, 2022, from https://machinelearningmastery.com/how-to-visualize-filters-and-feature-maps-in-convolutional-neural-networks/

Brownlee, J. (2022). How Do Convolutional Layers Work in Deep Learning Neural Networks?. Retrieved 9 May 2022, from https://machinelearningmastery.com/convolutional-layers-for-deep-learning-neural-networks/

Brownlee, J. (2022). How to Develop a CNN for MNIST Handwritten Digit Classification. Retrieved 9 May 2022, from https://machinelearningmastery.com/how-to-develop-a-convolutional-neural-network-from-scratch-for-mnist-handwritten-digit-classification/

