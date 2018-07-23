TensorFlow Examples This tutorial was designed for easily diving into TensorFlow, through examples. For readability, it includes both notebooks and source codes with explanation. It is suitable for beginners who want to find clear and concise examples about TensorFlow. Besides the traditional raw TensorFlow implementations, you can also find the latest TensorFlow API practices (such as layers, estimator, dataset, ...). Update (03/18/2018): TensorFlows Eager API examples available! (TF v1.5+ recommended). If you are using older TensorFlow version (0.11 and under), please have a look here. Tutorial index 0 - Prerequisite Introduction to Machine Learning. Introduction to MNIST Dataset. 1 - Introduction Hello World (notebook) (code). Very simple example to learn how to print "hello world" using TensorFlow. Basic Operations (notebook) (code). A simple example that cover TensorFlow basic operations. TensorFlow Eager API basics (notebook) (code). Get started with TensorFlows Eager API. 2 - Basic Models Linear Regression (notebook) (code). Implement a Linear Regression with TensorFlow. Linear Regression (eager api) (notebook) (code). Implement a Linear Regression using TensorFlows Eager API. Logistic Regression (notebook) (code). Implement a Logistic Regression with TensorFlow. Logistic Regression (eager api) (notebook) (code). Implement a Logistic Regression using TensorFlows Eager API. Nearest Neighbor (notebook) (code). Implement Nearest Neighbor algorithm with TensorFlow. K-Means (notebook) (code). Build a K-Means classifier with TensorFlow. Random Forest (notebook) (code). Build a Random Forest classifier with TensorFlow. 3 - Neural Networks Supervised Simple Neural Network (notebook) (code). Build a simple neural network (a.k.a Multi-layer Perceptron) to classify MNIST digits dataset. Raw TensorFlow implementation. Simple Neural Network (tf.layers/estimator api) (notebook) (code). Use TensorFlow layers and estimator API to build a simple neural network (a.k.a Multi-layer Perceptron) to classify MNIST digits dataset. Simple Neural Network (eager api) (notebook) (code). Use TensorFlow Eager API to build a simple neural network (a.k.a Multi-layer Perceptron) to classify MNIST digits dataset. Convolutional Neural Network (notebook) (code). Build a convolutional neural network to classify MNIST digits dataset. Raw TensorFlow implementation. Convolutional Neural Network (tf.layers/estimator api) (notebook) (code). Use TensorFlow layers and estimator API to build a convolutional neural network to classify MNIST digits dataset. Recurrent Neural Network (LSTM) (notebook) (code). Build a recurrent neural network (LSTM) to classify MNIST digits dataset. Bi-directional Recurrent Neural Network (LSTM) (notebook) (code). Build a bi-directional recurrent neural network (LSTM) to classify MNIST digits dataset. Dynamic Recurrent Neural Network (LSTM) (notebook) (code). Build a recurrent neural network (LSTM) that performs dynamic calculation to classify sequences of different length. Unsupervised Auto-Encoder (notebook) (code). Build an auto-encoder to encode an image to a lower dimension and re-construct it. Variational Auto-Encoder (notebook) (code). Build a variational auto-encoder (VAE), to encode and generate images from noise. GAN (Generative Adversarial Networks) (notebook) (code). Build a Generative Adversarial Network (GAN) to generate images from noise. DCGAN (Deep Convolutional Generative Adversarial Networks) (notebook) (code). Build a Deep Convolutional Generative Adversarial Network (DCGAN) to generate images from noise. 4 - Utilities Save and Restore a model (notebook) (code). Save and Restore a model with TensorFlow. Tensorboard - Graph and loss visualization (notebook) (code). Use Tensorboard to visualize the computation Graph and plot the loss. Tensorboard - Advanced visualization (notebook) (code). Going deeper into Tensorboard; visualize the variables, gradients, and more... 5 - Data Management Build an image dataset (notebook) (code). Build your own images dataset with TensorFlow data queues, from image folders or a dataset file. TensorFlow Dataset API (notebook) (code). Introducing TensorFlow Dataset API for optimizing the input data pipeline. 6 - Multi GPU Basic Operations on multi-GPU (notebook) (code). A simple example to introduce multi-GPU in TensorFlow. Train a Neural Network on multi-GPU (notebook) (code). A clear and simple TensorFlow implementation to train a convolutional neural network on multiple GPUs. Dataset Some examples require MNIST dataset for training and testing. Dont worry, this dataset will automatically be downloaded when running examples. MNIST is a database of handwritten digits, for a quick description of that dataset, you can check this notebook. Official Website: http://yann.lecun.com/exdb/mnist/ Installation To download all the examples, simply clone this repository: git clone https://github.com/aymericdamien/TensorFlow-Examples To run them, you also need the latest version of TensorFlow. To install it: pip install tensorflow or (if you want GPU support): pip install tensorflow_gpu For more details about TensorFlow installation, you can check TensorFlow Installation Guide More Examples The following examples are coming from TFLearn, a library that provides a simplified interface for TensorFlow. You can have a look, there are many examples and pre-built operations and layers. Tutorials TFLearn Quickstart. Learn the basics of TFLearn through a concrete machine learning task. Build and train a deep neural network classifier. Examples TFLearn Examples. A large collection of examples using TFLearn.