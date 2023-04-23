# insurance-fraudster-capstone-project
To predicting the “Fraud in auto insurance claims” 
# Problem Statement:
  The data that I have is from Automobile Insurance. I will be creating a predictive model that predicts if an insurance claim is fraudulent or not.
 # Business Case:
  claim related fraud is a huge problem in the insurance industry. It is quite complex and difficult to identify those unwanted claims. I am trying to troubleshoot and     help the General Insurance industry with this problem by using some Machine Learning Algorthims.
 # ROI : 
  A framework which will determine whether a customer claim is fraud or genuine from the given details.
  By accurately predicting which claims are likely to result in vehicle repairs rather than total losses, we can more effectively manage our vehicle repair supply chain   and reduce overall repair costs.
  By accurately predicting which auto insurance claims are fraudulent, we can reduce the number of fraudulent claims that are paid out, resulting in a significant cost     savings for the company.
# Machine Learning Problem :
   This business case comes under classification problem in Supervised Learning method.
   The features for the machine learning model include a variety of information related to the Demographic, Policy, Claim, Vehicle, Fraud information. The target             variable for the machine learning model would be a binary variable indicating whether or not the claim is fraudulent.
   Once we have identified the features and the target variable, we can start exploring and cleaning the data, engineering new features.
   Selecting an appropriate machine learning algorithm to train and test the model.
   Evaluating the Model.
   
# Dealing with Data : 
  Grouped the vehicle data through recursive grouping.
  after groped the data merging all given data on customer ID.
  
## Dropped unnecessary columns such are Ids ,country.
  As the whole data was recorded in 2015 at india only
  Country, year from IncidentDate were dropped
  CustomerID, PolicyNumber, IncidentAddress were dropped due to high cardinality and no effect on target.
  
# Feature Engineering : 
   Splitted DateofIncident,DateofPolicyCoverage columns into year, month, day columns
   Splitted policy_CombinedSingleLimit column to Singlelimit and combinedlimit through split(‘/’) string method.
   Created a vehicle_lifetime feature through (incident_Year – VehicleYOM)
   Created state_city feature using string concatenation of IncidentState, IncidentCity 
   Created netamount feature through (Capital_Gain + Capital_Loss)

# Visulisation : 
 ## Insights
  we use countplot for hobbies column, typeofincident, sevirtyofincident.
   #### Hobbies column  
    One thing which is striking in this graph is that people with chess and cross-fit as hobby have extremely high number of fraudulent claims.
   #### typeofincident
     Multi-vehicle and single vehicle collisions have more number of frauds compared to parked and vehicle theft. One of the reasons could be that in a collision,          there is high possibility of more damage to car, as well as the passengers and hence the need to file false insurance claims.
   #### sevirityofincident
     Here, compared to minor damage, total loss and trivial damage, fraudulent claims are highest in major damage. One of the reason could be that the high amount of        repair cost which will be incurred by the insurer due to major damage.   
# Preprocessing:
  ### Deal with missingvalues
   using missingno library to know how much of missing values are hear in data.
   #
    if simple imputer and Knn imputation is used to impute missing values.
 ### Deal with Outliers :
    if winsorisation Techinique is used to handle outliers.
     Winsorization is a technique used in statistics to limit the effect of outliers by capping the extreme values in a dataset.
 ### Dealing with target value 
   our target data is unbalanced data. so, we use SMOTE method to balanced the data
 
   ##### Ordinal encoding, Label encoding and One-hot encoding is used to convert categorical into numerical values.
 
 # Train-Test_spliting:
    The training set is used to fit the model, while the testing set is used to evaluate its performance. The main purpose of this technique is to check how well the        model can generalize to new, unseen data.
 # Standardisation : 
    Standardization is a technique used in data preprocessing to transform data to have zero mean and unit variance. It involves scaling the features of a dataset to        have a common scale, which helps in improving the accuracy and efficiency of machine learning models.

## Model building and validation. 
     
