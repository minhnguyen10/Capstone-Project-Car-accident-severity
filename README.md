# Capstone Project - Car accident severity
Capstone Project for IBM Data Science certificate

# 1. Introduction
According to Center for Disease Control and Prevention (CDC), Road traffic crashes are a leading cause of death in the United States for people aged 1–54. Since car is the major vehicle in the United State, it contribute the most to the road traffic acciedent. Morover, Road traffic accidents are also estimated to cost the US economy up to $871 billion in a single year according to the Administration of the USA. Specifically, According to 2015 WSDOT data, a crash occurs every 4.5 minutes and the number of Fatal collisions is 499 as well as 36,531 injury collisions in 2015, including number of injuries and the persons who were killed or injured. 

It seems obvious that the occurrence and severity of road traffic accidents will be related to several of factors including environmental conditions, driver responsbility, and other factors such as the angles and speeds of collision. Some factors seems potentially serve as good predictors of accident severity on their own. For example, weather condition, specially raining, might cause more accident to occur. 

We can begin to study data from past accidents to gain insight understanding of different factors that affects an accidents by looking at a accident reccord in Seattle. Using Machine Learning techniques to create models to predict the severity of future accidents. 

The two main stakeholders of building this kind of model are (1) Public Authority of Seattle, who may be able to use the result improve their road planning and traffic calming strategies and (3) drivers, who will be warned to avoid future accidents

# 2. Dataset
The dataset used for this project is a comprehensive dataset of 194,673 accidents occurring between 2004–present in the Seattle city area that could be obtain from [here](https://s3.us.cloud-object-storage.appdomain.cloud/cf-courses-data/CognitiveClass/DP0701EN/version-2/Data-Collisions.csv). The data contains the severity of each car accidents along with the time and conditions of the accident. Severity Code was the target of this project. It was in the form of 1 - Property Damage Only and 2 - Physical Injury, which are encoded to the form of 0 and 1 consecutively. 

### Feature selection:

**COLLISIONTYPE:**  Collision type  
**WEATHER:** A description of the weather conditions during the time of the collision  
**ROADCOND:** The condition of the road during the collision  
**LIGHTCOND:** The light conditions during the collision  
**INATTENTIONIND:** Whether or not collision was due to inattention. (Y/N)  
**UNDERINFL:** Whether or not a driver involved was under the influence of drugs or alcohol  
**SPEEDING:**  Whether or not speeding was a factor in the collision  
**SEVERITYCODE:** Target - A code that corresponds to the severity of the collision  
 

# 3. Methodology
## 3.1. Data Exploration
First of all, find the percentage of nan value in the chosen features. Here is the result
We can see that SPEEDING and INATTENTIONIND have a lot of nan value, so remove two columns as well row that have at least one nan value.
Next, for all other features, explore the value and remove rows that have "Unknown" or "Other" values.
Then for UNDERINFL, since it displayed two type of YES/No answer: "1", "0", "YES", "NO", change all value "YES" to "1" and "NO" to "0" to be consistent.
After that, one-hot-encoded the data set using get dummies
Finally, divide the dataset into training set (75%) and test set (25%)
## 3.2. Model Development and Evaluation

# 4.Result

# 5.Conclusion

# Sources
1. [https://www.cdc.gov/injury/features/global-road-safety/index.html](https://www.cdc.gov/injury/features/global-road-safety/index.html)
2. [https://www.wsdot.wa.gov/mapsdata/crash/pdf/2015_Annual_Collision_Summary.pdf](https://www.wsdot.wa.gov/mapsdata/crash/pdf/2015_Annual_Collision_Summary.pdf)
