#Neural_Network_Charity_Analysis
Neural Networks Week 19
# Neural_Network_Charity_Analysis
Working with Neural Network Models through Pandas in Python
## Overview of Neural_Network_Charity_Analysis:
Bek, just as you have has gone through a Data Analytics Bootcamp several years ago and now wants to test those skills again by working with you to build a neural network. Utilizing data provided to you by Alphabet Soup, they want to evaluate funds received from over 34,000 organizations and if their charity start-ups were successful. With the help of pandas Scikit-Learn’s StandardScaler, you will be preprocessing the data to get it ready to go through the neural network. Next, with your background of TensorFlow, we will design a neural network create a binary classification model that can predict if an Alphabet Soup–funded organization will be successful based on the features in the dataset. Finally, we will rerun through the model, optimizing it to reach an accuracy over 75%. 
#### The below pseudocode provided us an outline for the analysis ####
Deliverable 1: Preprocessing Data for a Neural Network Model
Deliverable 2: Compile, Train, and Evaluate the Model
Deliverable 3: Optimize the Model
Deliverable 4: A Written Report on the Neural Network Model

1.	## Deliverable 1: Preprocessing Data for a Neural Network Model:


![alttext](https://github.com/mbehr11/Neural_Network_Charity_Analysis/tree/main/Resources/application_df .PNG) 


2.	## Deliverable 2: Compile, Train, and Evaluate the Model:

![alttext](https://github.com/mbehr11/Neural_Network_Charity_Analysis/tree/main/Resources/compile_train&evaluate_model.PNG)

•	## Model_summary:

![alttext]( https://github.com/mbehr11/Neural_Network_Charity_Analysis/tree/main/Resources/model_summary.PNG)

•	### Compile model:

![alttext](https://github.com/mbehr11/Neural_Network_Charity_Analysis/tree/main/Resources/compile_model.PNG)


•	### Create a callback for every epoch:


![alttext](https://github.com/mbehr11/Neural_Network_Charity_Analysis/tree/main/Resources/callback_model.PNG)

•	### Train the model:

![alttext]( https://github.com/mbehr11/Neural_Network_Charity_Analysis/tree/main/Resources/train_model.PNG)

•	### Evaluate_model:

![alttext]( https://github.com/mbehr11/Neural_Network_Charity_Analysis/tree/main/Resources/evaluate_model.PNG)

•	### Export_model:

![alttext]( https://github.com/mbehr11/Neural_Network_Charity_Analysis/tree/main/Resources/export_model.PNG)


3.	## Deliverable 3: Optimize the Model:
•	### Adjusting the input data to ensure that there are no variables or outliers that are causing confusion in the model, such as:

![alttext](https://github.com/mbehr11/Neural_Network_Charity_Analysis/tree/main/Resources/dropped_EIN.PNG)

•	### Created a bin for names:

![alttext](https://github.com/mbehr11/Neural_Network_Charity_Analysis/tree/main/Resources/name_bin.PNG)

•	### Created a bin for application_type:

![alttext]( https://github.com/mbehr11/Neural_Network_Charity_Analysis/tree/main/Resources/application_type_bin.PNG)

•	### Create a bin for classification:

![alttext]( https://github.com/mbehr11/Neural_Network_Charity_Analysis/tree/main/Resources/classification_bin.PNG)

•	### Increasing or decreasing the number of values for each bin:

![alttext]( https://github.com/mbehr11/Neural_Network_Charity_Analysis/tree/main/Resources/increase_namecounts.PNG)

![alttext]( https://github.com/mbehr11/Neural_Network_Charity_Analysis/tree/main/Resources/lessthan5_name_counts.PNG)

•	### Adding more neurons to a hidden layer:

![alttext]( https://github.com/mbehr11/Neural_Network_Charity_Analysis/tree/main/Resources/addmore_neurons. PNG)



•	### Adding more hidden layers.


![alttext](https://github.com/mbehr11/Neural_Network_Charity_Analysis/tree/main/Resources/third_layer. PNG)

•	### Evaluate the model after optimization:

![alttext](https://github.com/mbehr11/Neural_Network_Charity_Analysis/tree/main/Resources/evaluate_model_test2. PNG)

4.	## Deliverable 4: A Written Report on the Neural Network Model:

### Data Preprocessing:
•	What variable(s) are considered the target(s) for your model?
The variable that was considered the target for the column “Is-Successful”. This determined that the money requested was used for its intended purpose based on the application. 
•	What variable(s) are considered to be the features for your model?
The variables that are features for the model are: NAME, APPLICATION_TYPE, AFFILATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, SPECIAL_CONSIDERATIONS, STATUS, AND ASK_AMT.
•	What variable(s) are neither targets nor features, and should be removed from the input data?
•	When running this model, the EIN variable column was dropped because the model could confuse the numbers as data input which would alter the accuracy result and cause overfitting in the model. 

### Compiling, Training, and Evaluating the Model
•	How many neurons, layers, and activation functions did you select for your neural network model, and why?
For the first model there were 2 layers. The first layer was 80 and the second layer was 30. I used relu for the first two layers and sigmoid for the outer layers for the activation functions. I played around with the numbers and activations functions, but this put my accuracy at around 72%
•	Were you able to achieve the target model performance?
Yes.
•	What steps did you take to try and increase model performance?
To increase model performance, I only removed the EIN column. Then I created two more bins for NAME and CLASSIFICATION. I also played around with the counts of NAME AND CLASSIFICATION, testing which values to replace if counts are less than or equal to 5 and how many name counts are greater than 5? I then increased my first layer of neurons to 100, the second layer stayed at 30, and I added a third layer at 10. I also used sigmoid activation function instead of relu. 
## Summary: 
After optimizing my model, I was able to move the accuracy from 72% to 78%. An application would be able to increase success if their name or application showed up more than 5 times. The more applications the more success. The application type needed to fall under: T3, T4, T5, T6, T8, T10, and T19. 

I would try the Random Forest Classifier as it can handle a large set of data and categorize it into simple yes or no questions and or 1 and 0. This will make the organization for the model much cleaner. 

## Contributing 
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)

