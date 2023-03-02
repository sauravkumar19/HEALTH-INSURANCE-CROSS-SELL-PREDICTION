# HEALTH-INSURANCE-CROSS-SELL-PREDICTION
Problem Statement
Our client is an Insurance company that has provided Health Insurance to its customers now they need your help in building a model to predict whether the policyholders (customers) from past year will also be interested in Vehicle Insurance provided by the company.

An insurance policy is an arrangement by which a company undertakes to provide a guarantee of compensation for specified loss, damage, illness, or death in return for the payment of a specified premium. A premium is a sum of money that the customer needs to pay regularly to an insurance company for this guarantee.

For example, you may pay a premium of Rs. 5000 each year for a health insurance cover of Rs. 200,000/- so that if, God forbid, you fall ill and need to be hospitalised in that year, the insurance provider company will bear the cost of hospitalisation etc. for upto Rs. 200,000. Now if you are wondering how can company bear such high hospitalisation cost when it charges a premium of only Rs. 5000/-, that is where the concept of probabilities comes in picture. For example, like you, there may be 100 customers who would be paying a premium of Rs. 5000 every year, but only a few of them (say 2-3) would get hospitalised that year and not everyone. This way everyone shares the risk of everyone else.

Just like medical insurance, there is vehicle insurance where every year customer needs to pay a premium of certain amount to insurance provider company so that in case of unfortunate accident by the vehicle, the insurance provider company will provide a compensation (called ‘sum assured’) to the customer.

Building a model to predict whether a customer would be interested in Vehicle Insurance is extremely helpful for the company because it can then accordingly plan its communication strategy to reach out to those customers and optimise its business model and revenue.

Now, in order to predict, whether the customer would be interested in Vehicle insurance, you have information about demographics (gender, age, region code type), Vehicles (Vehicle Age, Damage), Policy (Premium, sourcing channel) etc.


Attribute Information

id : Unique ID for the customer

Gender : Gender of the customer

Age : Age of the customer

Driving_License 0 : Customer does not have DL, 1 : Customer already has DL

Region_Code : Unique code for the region of the customer

Previously_Insured : 1 : Customer already has Vehicle Insurance, 0 : Customer doesn't have Vehicle Insurance

Vehicle_Age : Age of the Vehicle

Vehicle_Damage :1 : Customer got his/her vehicle damaged in the past. 0 : Customer didn't get his/her vehicle damaged in the past.

Annual_Premium : The amount customer needs to pay as premium in the year

PolicySalesChannel : Anonymized Code for the channel of outreaching to the customer ie. Different Agents, Over Mail, Over Phone, In Person, etc.

Vintage : Number of Days, Customer has been associated with the company

Response : 1 : Customer is interested in vehicle insurance policy, 0 : Customer is not interested in vehicle insurance policy


Conclusion

● Vehicle_damage, Vehicle_age and channel response feature were found to
be most relevant for Classify the insurance response for company.
● From vehicle_damage and vehicle age, one can notice people have to pay
higher premium for insurance if there car get damage previously or there car
is older than 2 years. Also response rate of insurance is also high for such
scenario.
● For random forest channel response, Annual premium and Vehicle_damage
are important feature for classification.
● For XGB Vehicle_damage, Age section and gender are important feature for
classification.
● Logistic regression model does not perform good in this dataset as very few
dependent variable is strongly correlated to independent variable. The XGB
and GBM provide substantial improvement in predicting the insurance
response.The accuracy and roc_auc score is greater than 0.9 for both model.
● Random forest model precision score is 0.91 while recall score is 0.77. This
means random forest gives good result for positive insurance response.
● So we used XGboost model for classification. This model can also improve by
finer tuning of hyperparameters.
