# ARTIFICIAL NEURAL NETWORK
 Prediction of air particle values

 The purpose of this application is to estimate the weather monitoring parameters determined for the future periods by using the weather monitoring values ​​of the past periods with the help of artificial neural networks. If we want to analyze these data while we have the data of the past period and to estimate the output value corresponding to these values ​​according to the relationship between them, we can choose to use the feed forward - back propagation artificial neural network, which is one of the artificial neural network models. By creating variables such as the number of neurons and learning function related to this artificial neural network architecture by trial and error method, we configure it in the best way according to the data to be used. Based on the smallest error value, we make predictions with the artificial neural network of the selected feature. Necessary evaluations about the application are made by comparing the obtained values ​​with the actual values.



 Feed Forward - Back Propagation Artificial Neural Network Architecture

The way neurons, which are the elements that make up feed-forward networks, come together are not random. In order to perform their functions in artificial neural networks, neurons are positioned in 3 different layers and the neurons in each layer are parallel to each other.






1) Input Layer: The input layer, which is the first layer of a feed-forward – back-emitted artificial neural network, is the layer that provides input from outside. If there are many inputs to be learned, this layer should contain that number of neurons. The inputs received from the outside are transferred to the next layer, the hidden layer, without any processing.
2) Hidden Layers: In feed-forward – back-propagation artificial neural networks, the hidden layer is the layer in which the inputs are processed with a function after multiplying with the weights. The number of neurons on the layer can vary from problem to problem. In these layers, forward calculations and backward error propagation are performed.
3) Output Layer: It is the layer where the class information or label value of the samples to be learned in the artificial network is calculated as output.




Air temperature, precipitation amount and particulate matter data measured at Adana - Doğankent weather measurement station between 01.01.2019 - 01.11.2019 were used as input values ​​in the training dataset for the application of weather forecasting with artificial neural networks.
As the target value in the training data set, the sulfur dioxide data measured at Adana - Doğankent air measurement station between 01.01.2019 - 01.11.2019 was used.
The input values ​​that the artificial neural network trained with these data will use in making predictions are the air temperature, precipitation amount and particulate matter data measured at Adana - Doğankent weather measurement station between 01.11.2019 - 30.11.2019. The actual sulfur dioxide values ​​to be compared with the sulfur dioxide forecast values ​​obtained as a result of the estimation to be made are the sulfur dioxide data measured at Adana - Doğankent weather measurement station between 01.11.2019 - 30.11.2019.
All data used in the application were obtained from the Ministry of Environment and Urbanization - National Air Quality Monitoring Network - Continuous Monitoring Center.



The Neural Net Fitting module in the APPS menu of MATLAB was used to create the artificial neural network. In estimation problems with the Neural Net Fitting module, you want a neural network to be mapped between a numerical input dataset and a set of numerical targets. Examples of such problems are estimating engine emission levels based on fuel consumption and speed measurements, or estimating a patient's body fat level based on body measurements. The Neural Fitting app will allow us to select data, build and train a network, and evaluate its performance using mean square error and regression analysis.



Step 1: The Neural Network Fitting module is opened from the APPS menu of the MATLAB program. The screenshot of the login screen of the Neural Network Fitting module is shown below. On the login screen, click the next button. With the Next button, it proceeds to the select data screen where the input and target values ​​will be selected.


Step 2: In the Select data screen, input values ​​and target values ​​to be used as training data are entered into the program. Excel files containing the data are selected and next is pressed.


Step 3: The screen where we will decide what percentage of the training set data obtained in the previous step will be used in training, what percentage will be used in validation and what percentage will be used in the testing process opens. The default values ​​on this screen are 70% training, 15% validation and 15% testing. However, as a result of the trials, it was seen that the 15% data set reserved for the validation process is more and the network works better when this value is 10%.


Step 4: In this step, the number of neurons is selected to create the network architecture. The number of neurons was determined as 5 neurons as a result of the experiments. At the same time, in this step, there is an overview of the architecture of the network. The artificial neural network is a network that calculates 1 output value in response to 3 inputs, consists of a hidden layer and has 5 neurons in this layer and 1 neuron in the output layer.



Step 5: The completed network trains by selecting a training function. Network training is started by choosing the Levenberg – Marquardt algorithm, which is the fastest of the training functions. After the network training process, the correlation between the data of the network, the square of the errors and the statistics of the test are calculated. The closer the R value to be calculated is to 1, the more successful the training process is. The network can be trained again until the desired R value is reached.



Step 6: The values ​​obtained as a result of the network training processes are examined. If the values ​​are in an acceptable range, the operations are continued. As a result of the training processes, it has been seen that the values ​​of the network can explain about 70% of the change in the data, and this is an acceptable range. At the same time, the network can also make predictions with an accuracy close to 70%. The regression tables of the network are shown below.


The training parameters of the artificial neural network are shown below.

Error values ​​of artificial neural networks are shown below.

The histogram of the error values ​​of the artificial neural network is shown below.




Results and Discussion

When Levenberg-Marquardt is selected as the training algorithm, the feedforward-backpropagation artificial neural network can predict approximately 70% of the desired values ​​with 1 hidden layer and 5 neurons in this layer. This rate is above an acceptable margin of error in terms of weather forecasting. In the working principle of the artificial neural network, there is an understanding of examining the data and making sense of the changes in the data. The reason why the artificial neural network makes predictions at this accuracy rate may be due to the insufficient degree of relationship between the data. It is possible to obtain better results with a data set with more correlations and less deviation values.



