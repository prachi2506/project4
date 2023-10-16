### ✈️ Flight Delay Prediction ✈️
## Our project focuses on predicting flight delays in American Airlines using machine learning techniques. 
The dataset is sourced from Kaggle. Data included information regarding arrival time, scheduled time, weather information, and cancellation reasons. The data was cleaned thoroughly and we dropped 13 unnecessary columns for our data analysis.
- The objective of this project is to predict flight delays in advance.
### Cleaning
Original file size 500+ MB which includes 14 airlines and each has at least 60k data
We chose American Airlines Lnc. to make the dataset smaller so we can run the code properly. We used SQL to drop the columns and clean the data as per requirements.

### Visualizations
To create visualizations we used Tableau and determined what airports have the highest and lowest rate of cancelations using a Pie chart. Bar chart helped us to visualize which day of the week has the maximum number of flight cancelations. 

### Machine learning
  After plenty of trial and error, we decided to use a neural network model that utilizes the make circles module from sk.learn.
The model yielded the highest accuracy of all our attempts. We started with running a decision tree model, with which we were only able to acheive 66% accuracy. When trying to optimize the model we found that no matter how and what we trained and tested within the model it was not affecting the accuracy of the model. This indicated to us that there was either something wrong, or this was simply not the most effective solution to our problem.     
![MakeCircles](Output_screenshots/get_circles.png)
We moved onto a neural network model and got to work. We utilized make circles from sk.learn to classify and visualize the test data. At first we started with a larger sample set of data because our data set is large itself, but we found that keeping the sample set at 1000 was most accurate. I also took the time to experiment with switching out the variables for the dummy data. Of all the combinations, using arrival_delay, departure_delay and distance provided the best outcome. Keras tuner was also a useful tool that we used to decide the activation function as well as the number of neurons in each layer. 
![KerasTuner](Output_screenshots/keras_tuner_decide.png)
We also utilized keras tuner to get the top 3 model hyperparameters and evaluate those models against the test data. 
![BestHyperparameters](Output_screenshots/best_models_3.png)
After using keras tuner to get the three best hyperparameters, we evaluated the best option against the full dataset and printed the output. 
![FinalModel](Output_screenshots/final_model.png)

### Conclusion
  When starting the project we asked ourselves ‘what machine learning method would be the best for accurately predicting flight delays?’. We quickly got to work analyzing the problem and parameters and realized we had lots of options. Through trial and error we were able to narrow down our list of models to one neural networking model that achieved the highest accuracy of all our tests - 97%
  By using a FeedForward Neural Networking model we were able to build a model that could use the dataset provided to predict whether a flight with American Airline is likely to be delayed or not at a rate of 97% effectiveness.
