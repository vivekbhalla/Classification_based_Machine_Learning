Classification Based Machine Learning
=====================================

This project is to implement and evaluate multi-class classification algorithms on handwritten digit and recognize the digit among the ten digits (0-9).

Each sample of a handwritten digit consists of 512 features.
The training dataset contains approximately 2000 samples for each digit, whereas the testing dataset consists of 150 samples of each digit.
The ground truth is a 10 element row vector in which if the first element value is 1 and all others are zero then it belongs to digit 0 i.e. class 1, similarly if the second element is 1 and others are zero then it belongs to digit 1 i.e. class 2 and so on till digit 9 i.e. class 10.
The training data is further decomposed and divided into a training and validation dataset. This new training data set is 80% of the original training dataset and the validation dataset is the remaining 20%. 

The training phase calculates the trained weights (train\_\*.m). These weights are used by the validation dataset to predict the classes, and looking at the Error rate of the validation phase the parameters in the training phase are adjusted to get best results i.e. the least error. Finally after the best results are obtained these weights are used to predict classes for the test dataset and the final error and class outputs of this dataset are calculated and reported (test_*.m). 

Three different classifiers were used for this project. The first classifier was Logistic Regression using Softmax functions (train_lr.m & test_lr.m). The second classifier used was Neural Network, with Sigmoid activation function for hidden layers and Softmax activation function for output layer (train_nn.m & test_nn.m). The third classification model was implemented by using MATLAB’s Neural Network toolbox (nn_model.m).
 
The best performance for the Logistic Regression Classifier was observed by setting the Learning Rate alpha = 0.001, Regularization Factor lambda = 0 (i.e. no regularization) and Number of Iterations = 266, which gave a % Error Rate of 2.9333 

The best performance for the Neural Network Classifier was observed by setting the Learning Rate alpha = 0.1 and Number of Iterations = 18, which gave a % Error Rate of 2.1333 

The best performance for the Neural Network Model (MATLAB) was observed by setting the Number of Hidden Neurons to be 40, which gave a % Error Rate of 2.466667 

Among all the three classification methods used, the Neural Network Classifier performed the best overall and gave the least error rate.

Note: The final output after training and testing for the test dataset are provided in the files named classes\_\*.txt for the respective classifiers (lr, nn, nn_model).
