# Bike_Sharing_Project_Using_NN

 Neural Network developed during my Deep Learning Fundamentals Nanodegree at Udacity. In this project, I created a simple neural network to use it to predict daily bike rental ridership.
 
 I’ve built my own neural network from scratch in my_answers.py file (later on, the file content is imported to my notebook).

Firstly, I created Neural Network class with the init function acommodating the number of input, hidden and output nodes. Next, I initialized the weights, defined the activation function and learning rate.

The values for hidden, output nodes, number of iterations and the learning rate are being set later and can be modified until we get the desired accuracy.

Then, I defined the train function that includes the feed-forward pass, backpropagation, the weights update after each iteration and a run function. All these functions are defined after the train function. In the notebook I started by cleaning and organizing the data, then splitting them into training, test and validation datasets. Next, NN class instance is being created with the input values and hyperparameters passed as arguments.
 
# Prerequisites
 1. Python 3.7
 2. Numpy (win-64 v1.15.4)
 3. Pandas (win-64 v0.23.4)
 4. Matplotlib (win-64 v3.0.2)
 5. Jupyter Notebook
 
# Getting Started

  This Bike-Sharing-Dataset has the number of riders for each hour of each day from January 1 2011 to December 31 2012. The number of riders is split between casual and registered, summed up in the cnt column. 
  Below is a plot showing the number of bike riders over the first 10 days or so in the data set. (Some days don't have exactly 24 entries in the data set, so it's not exactly 10 days.) You can see the hourly rentals here. This data is pretty complicated! The weekends have lower over all ridership and there are spikes when people are biking to and from work during the week. Looking at the data above, we also have information about temperature, humidity, and windspeed, all of these likely affecting the number of riders. You'll be trying to capture all this with your model.
  
  
![dataset](https://user-images.githubusercontent.com/55234691/89716685-b915f080-d9cc-11ea-81d7-9a9fe025e753.png)

# Results


The project meets the specifications, which are:


    1. All the code in the notebook runs in Python 3 without failing, and all unit tests pass.
    2. The sigmoid activation function is implemented correctly
    3. The forward pass is correctly implemented for the network's training.
    4. The run method correctly produces the desired regression output for the neural network.
    5. The network correctly implements the backward pass for each batch, correctly updating the weight change.
    6. Updates to both the input-to-hidden and hidden-to-output weights are implemented correctly.
    7. The number of epochs is chosen such the network is trained well enough to accurately make predictions but is not overfitting to the training data.
    8. The number of hidden units is chosen such that the network is able to accurately predict the number of bike riders, is able to generalize, and is not       overfitting.
    9 .The learning rate is chosen such that the network successfully converges, but is still time efficient.
    10. The number of output nodes is properly selected to solve the desired problem.
    11. The training loss is below 0.07 and the validation loss is below 0.13.

# Checkout the training results

    Progress: 100.0% ... Training loss: 0.076 ... Validation loss: 0.137
    
<img width="600" height="400"  alt="download (1)" src="https://user-images.githubusercontent.com/55234691/89716841-30984f80-d9ce-11ea-9c7e-f1eaa5e0c637.png">

# Checkout the prediction results

I use the test data to show how well the neural network is modeling the data.

<img width="600" height="400" alt="download" src="https://user-images.githubusercontent.com/55234691/89717023-f7f97580-d9cf-11ea-8291-8ba6a8c68704.png">

With the use of training and validation losses we can see how the model performs during the iterations. I end up with validation loss at 0.13 vs the training one at 0.07 which means that our model is overfitting - generalizing the pattern of the first two-thirds of the month on the last third of the month.
