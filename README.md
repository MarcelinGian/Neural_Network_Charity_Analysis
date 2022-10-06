# Neural_Network_Charity_Analysis
###Using Neural Networks & Machine Learning to predict whether applicants will be successful if funded by the "Alphabet Soup" organization. 

***
### Data Preprocessing:
- The data was split into features and target arrays
  - The "IS_SUCCESSFUL" Column was used as the target variable for my model
  - The "EIN" and "NAME" columnsn were removed, not considered targets nor fearures
  - All other variables were considered features during initial analysis
- Columns with more than 10 unique values were grouped together
- Categorical variables were encoded using one-hot encoding
- The numerical values were standardized using the StandardScaler() module 
- The preprocessed data was split into training and testing datasets

***
### Compiling, Training, and Evaluating the Model:
- My Initial Model contained 2 hidden layers
  - 80 Neurons in Layer 1 & 30 Neurons in Layer 2
  - The ReLU activation function was used for both hidden layers
 - The Sigmoid activation function was used for the output layer
 - The model was trained with 50 epochs
![01CompileTrainTest](https://user-images.githubusercontent.com/105818879/194007471-86e3bfc1-ffe5-4b81-a1c2-2281b9ec9894.png)

### Result:
#### This model was unable to achieve the target performance of Accuracy >= 75%
![02AccuracyScore](https://user-images.githubusercontent.com/105818879/194008090-d5bd8106-27ee-4bd2-b89a-af5efa612cb9.png)

***
## Optomization: 
### Attempt 1 - Adding More Neurons to the Hidden Layers 
![03Attempt1](https://user-images.githubusercontent.com/105818879/194189702-9f126e7e-6196-4932-8cf7-7bc238705cd6.png)
- #### Result:
  - Slight Decrease of Accuracy. Unable to achieve the target performance of Accuracy >= 75%
![04A1accuracy](https://user-images.githubusercontent.com/105818879/194010044-eda106c9-2774-441c-af13-b4d45318ca6f.png)

#### Attempt 2 - Increasing Amount of Epochs to the Training Regimen
- All other variables remained the same
![05Attempt2](https://user-images.githubusercontent.com/105818879/194011190-3755a516-1938-4a0f-8122-c817ed30f4c6.png)
- #### Result:
  - Slight Decrease of Accuracy. Unable to achieve the target performance of Accuracy >= 75%
![06A2accuracy](https://user-images.githubusercontent.com/105818879/194011246-e48b79e7-9b3b-42df-8990-d74867aa5042.png)

#### Attempt 3 
- Remove noisy variables
  - Several combinations were attempted
- Add more neurons to the hidden layers
- Add more hidden layers
- Change activation functions
![07Variables](https://user-images.githubusercontent.com/105818879/194012487-949f9c13-3d78-4ffc-9641-cfbbd290eb0c.png)
![08Attempt3](https://user-images.githubusercontent.com/105818879/194012539-d6851781-4e89-4e35-bee2-521d68c49ca6.png)
- #### Result:
  - Slight Increase in Accuracy. Unable to achieve the target performance of Accuracy >= 75%
![09A3accuracy](https://user-images.githubusercontent.com/105818879/194012577-e9717952-f6b4-4d8e-a244-645360edb9a9.png)

***
### Summary:
#### My initial model, as well as my 3 attempts at optomization, maintained it's accuracy score of about 72.5%. Higher accuracy may be achievable via the process of further binning columns that contain rarely occuring data points or removing variables from the dataset that could be considered "noisy".
