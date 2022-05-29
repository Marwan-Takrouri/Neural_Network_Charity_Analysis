# Neural_Network_Charity_Analysis
***The Purpose of the Analysis :***

***Overview :***

Beks has come a long way since her first day at that boot camp five years ago—and since earlier this week, when she started learning about neural networks! Now, she is finally ready to put her skills to work to help the foundation predict where to make investments.
With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.
From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years.

With my knowledge of machine learning and neural networks, i’ll be helping Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:
•	EIN and NAME—Identification columns
•	APPLICATION_TYPE—Alphabet Soup application type
•	AFFILIATION—Affiliated sector of industry
•	CLASSIFICATION—Government organization classification
•	USE_CASE—Use case for funding
•	ORGANIZATION—Organization type
•	STATUS—Active status
•	INCOME_AMT—Income classification
•	SPECIAL_CONSIDERATIONS—Special consideration for application
•	ASK_AMT—Funding amount requested
•	IS_SUCCESSFUL—Was the money used effectively


Neural networks (also known as artificial neural networks, or ANN) are a set of algorithms that are modeled after the human brain. They are an advanced form of machine learning that recognizes patterns and features in input data and provides a clear quantitative output. In its simplest form, a neural network contains layers of neurons, which perform individual computations. These computations are connected and weighed against one another until the neurons reach the final layer, which returns a numerical result, or an encoded categorical result.

Neural networks are particularly useful in data science because they serve multiple purposes.
One way to use a neural network model is to create a classification algorithm that determines if an input belongs in one category versus another. Alternatively neural network models can behave like a regression model, where a dependent output variable can be predicted from independent input variables. Therefore, neural network models can be an alternative to many of the models we have learned throughout the course, such as random forest, logistic regression, or multiple linear regression.
There are a number of advantages to using a neural network instead of a traditional statistical or machine learning model. For instance, neural networks are effective at detecting complex, nonlinear relationships. Additionally, neural networks have greater tolerance for messy data and can learn to ignore noisy characteristics in data. The two biggest disadvantages to using a neural network model are that the layers of neurons are often too complex to dissect and understand (creating a black box problem), and neural networks are prone to overfitting (characterizing the training data so well that it does not generalize to test data effectively). However, both of the disadvantages can be mitigated and accounted for.

Neural networks have many practical uses across multiple industries. In the finance industry, neural networks are used to detect fraud as well as trends in the stock market. Retailers like Amazon and Apple are using neural networks to classify their consumers to provide targeted marketing as well as behavior training for robotic control systems. Due to the ease of implementation, neural networks also can be used by small businesses and for personal use to make more cost-effective decisions on investing and purchasing business materials. Neural networks are scalable and effective—it is no wonder why they are so popular.
Brain metaphors, easy to use, and cost-effective? Excellent at detecting complex, nonlinear relationships? Neural networks are starting to sound like a great fit for the model. Beks sends Andy a quick Slack message to let him know the research phase of the project is well under way. Her next step will be to dig into the math a bit: What exactly goes into a neural network? To explore this, she'll start with the perceptron model.
Although artificial neural networks have become popular in recent years, the original design for computational neurons (and, subsequently, the neural network) dates as far back as the late 1950s, when Frank Rosenblatt, a pioneer in the field of artificial intelligence, created the perceptron, a machine for training the first neural network. The perceptron model is a single neural network unit, and it mimics a biological neuron by receiving input data, weighing the information, and producing a clear output.

***Results***


***Data Preprocessing***

o	What variable(s) are considered the target(s) for your model?

Answer :  IS_SUCCESSFUL column is my target .

o	What variable(s) are considered to be the features for your model?

Answer :Everything was featured except the EIN and NAMEs and I have dropped the column of Special Consideration on my attempts to increase the accuracy , but it didn’t affect my accuracy on the evaluate stage .

o	What variable(s) are neither targets nor features, and should be removed from the input data?

Answer :EIN and NAMEs


•	Compiling, Training, and Evaluating the Model

o	How many neurons, layers, and activation functions did you select for your neural network model, and why?

Answer : In the first neural network model I  performed 8 In the hidden_nodes_layer1 and 5 in the hidden_nodes_layer2.For the 1st & 2nd hidden layer the activation was “relu”, while in the Output layer we used “Sigmoid”. The total parameters were 403.
We used 100 epochs to train the module. The accuracy was 53% and the loss was 70%


o	Were you able to achieve the target model performance?

Answer: I was not able to achieve in fact no mater what I did my accuracy kept on getting lower starting in the optimization and then the 3 attempts after that , It dropped to 53% accuracy .

o	What steps did you take to try and increase model performance?

***Answer :***

I followed three attempts as below :.

First time in optimization I changed the my epochs=150, hidden_nodes_layer1 =  2000 and hidden_nodes_layer2 =100 , my parameters were 29,001 but my accuracy remained 53%.

second  attempt I dropped the column Special _Consideration ,  my epochs=150, hidden_nodes_layer1 =  190 and hidden_nodes_layer2 = 50 , my parameters were 17,581 but my accuracy remained 53%.

Third  attempt I dropped special consideration and  I changed the my epochs=50, hidden_nodes_layer1 =  90 and hidden_nodes_layer2 = 50 , my parameters were 8,381 but my accuracy remained 53%.



My Recommendation for improvement of accuracy will be :

There are a few means of optimizing a neural network:
•	Check out your input dataset.
•	Add more neurons to a hidden layer.
•	Add additional hidden layers.
•	Use a different activation function for the hidden layers.
•	Add additional epochs to the training regimen.


At last, our data is preprocessed and separated and ready for modelling. For our purposes, we will use the same framework we used for our basic neural network:
•	For our input layer, we must add the number of input features equal to the number of variables in our feature DataFrame.
•	In our hidden layers, our deep learning model structure will be slightly different—we'll add two hidden layers with only a few neurons in each layer. To create the second hidden layer, we'll add another Keras Dense class while defining our model. All of our hidden layers will use the relu activation function to identify nonlinear characteristics from the input values.
•	In the output layer, we'll use the same parameters from our basic neural network including the sigmoid activation function. The sigmoid activation function will help us predict the probability that an employee is at risk for attrition.






