# F21DL_Coursework_grp2

## Airline Survey Analysis

### Group Information
- **Group Name**: Dubai_PG 2 Dubai_PG
- **Project Title**: Airline Survey Analysis
- **Group Members**:
  - Danish Mariam
  - Kanjookaran Anugraha Antoo
  - Onafeso Fiyifoluwa
  - PAIDIMARRI AJAY
  - Hariharakumar Rathianr

### Research Objectives
1. **Objective 1**: Predict the level of satisfaction a passenger will have based on their ratings for services like Seat comfort, Food and drink, In-flight Wifi, Baggage handling, etc.
2. **Objective 2**: Identify which service areas (e.g., Food and drink, In-flight entertainment, Cleanliness, etc.) correlate most with lower satisfaction scores, and provide actionable insights for improvement.
3. **Objective 3**: Determine whether factors like age, gender, or customer type (First-time vs Returning customers) result in different satisfaction levels. Cluster the data based on the data.
4. **Objective 4**: Determine the satisfaction outcome based on the image of a person taking the survey.

### Project Milestones
- **R1**: Project Direction and Questions (Week 1 & 2)
  - Define clear objectives and hypotheses (e.g., key factors influencing satisfaction).
  - Complete initial exploratory data analysis and problem identification.
  
- **R2**: Data Analysis and Preprocessing (Week 3 & 4)
  - Perform data cleaning, handle missing values and transform features.
  - Visualize relationships and identify important patterns.
  
- **R3**: Clustering (Week 4 & 5)
  - Use clustering algorithms to segment passengers based on similar characteristics and satisfaction levels.
  - Evaluate clustering results using silhouette scores.
  
- **R4**: Baseline Training and Evaluation (Week 6 & 7)
  - Train three machine learning models: Decision Tree, K-Nearest Neighbors (KNN), and Naive Bayes for classification.
  - Evaluate models using accuracy, precision, recall, and F1-score.
  
- **R5**: Neural Networks (Week 8 & 9)
  - Implement Multi-Layer Perceptron (MLP), CNN, SGD for satisfaction prediction.
  - Fine-tune the model and compare its performance with the baseline models.

### Dataset Information
- **Source of Dataset(s)**:
  - [Airline Passenger Satisfaction Dataset](https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction/data)
     - True Source: https://www.kaggle.com/datasets/johndddddd/customer-satisfaction
     - License: unknown
     - File name: airline_passenger_satisfaction.csv
  - [Airline Passenger Satisfaction (Alternative)](https://www.kaggle.com/datasets/mysarahmadbhat/airline-passenger-satisfaction/data)
     -  True Source: https://creativecommons.org/publicdomain/zero/1.0/
     -  License: No Copyright
     -  File Name: train.csv & test.scv
  - [VGGFace2 Dataset](https://www.kaggle.com/datasets/jonathanoheix/face-expression-recognition-dataset)
     -  True Source: Unknown
     -  License: Unknown
     -  Folder name: "train" & "Validate" folders
  
- **True Source**: Data is taken from Kaggle
- **Examples from Dataset**:
  - **Example 1**:
         #   Column                                  Non-Null Count   Dtype  
        ---  ------                                  --------------   -----  
         0   ID                                      129880 non-null  int64  
         1   Gender                                  129880 non-null  object 
         2   Age                                     129880 non-null  int64  
         3   Customer Type                           129880 non-null  object 
         4   Type of Travel                          129880 non-null  object 
         5   Class                                   129880 non-null  object 
         6   Flight Distance                         129880 non-null  int64  
         7   Departure Delay                         129880 non-null  int64  
         8   Arrival Delay                           129487 non-null  float64
         9   Departure and Arrival Time Convenience  129880 non-null  int64  
         10  Ease of Online Booking                  129880 non-null  int64  
         11  Check-in Service                        129880 non-null  int64  
         12  Online Boarding                         129880 non-null  int64  
         13  Gate Location                           129880 non-null  int64  
         14  On-board Service                        129880 non-null  int64  
         15  Seat Comfort                            129880 non-null  int64  
         16  Leg Room Service                        129880 non-null  int64  
         17  Cleanliness                             129880 non-null  int64  
         18  Food and Drink                          129880 non-null  int64  
         19  In-flight Service                       129880 non-null  int64  
         20  In-flight Wifi Service                  129880 non-null  int64  
         21  In-flight Entertainment                 129880 non-null  int64  
         22  Baggage Handling                        129880 non-null  int64  
         23  Satisfaction                            129880 non-null  object 
  - **Example 2**:
        Data columns (total 25 columns):
         #   Column                             Non-Null Count   Dtype  
        ---  ------                             --------------   -----  
         0   Unnamed: 0                         103904 non-null  int64  
         1   id                                 103904 non-null  int64  
         2   Gender                             103904 non-null  object 
         3   Customer Type                      103904 non-null  object 
         4   Age                                103904 non-null  int64  
         5   Type of Travel                     103904 non-null  object 
         6   Class                              103904 non-null  object 
         7   Flight Distance                    103904 non-null  int64  
         8   Inflight wifi service              103904 non-null  int64  
         9   Departure/Arrival time convenient  103904 non-null  int64  
         10  Ease of Online booking             103904 non-null  int64  
         11  Gate location                      103904 non-null  int64  
         12  Food and drink                     103904 non-null  int64  
         13  Online boarding                    103904 non-null  int64  
         14  Seat comfort                       103904 non-null  int64  
         15  Inflight entertainment             103904 non-null  int64  
         16  On-board service                   103904 non-null  int64  
         17  Leg room service                   103904 non-null  int64  
         18  Baggage handling                   103904 non-null  int64  
         19  Checkin service                    103904 non-null  int64  
         20  Inflight service                   103904 non-null  int64  
         21  Cleanliness                        103904 non-null  int64  
         22  Departure Delay in Minutes         103904 non-null  int64  
         23  Arrival Delay in Minutes           103594 non-null  float64
         24  satisfaction                       103904 non-null  object 
  
- **Additional Steps**:
  - Arrival Delay column contains null values.
  - Mean values is taken for filling the null values in this dataset

### Requirement Descriptions (R2–R5)
- **R2**: **Prediction Outputs**:  
- **R3**: **Prediction Inputs**: 
- **R4/R5**: **Results**:

  **Tabular Data**
  ![image](https://github.com/user-attachments/assets/3bb82fa7-c30f-4468-96a3-0906ba15354f)
Analysis Using Keras Perceptron Function with 10-Fold Cross-Validation and Evaluation Metrics
When validation is performed across the entire dataset, it gives an accuracy of 94%; as against 91% by cross-validation on the selected feature set.

![image](https://github.com/user-attachments/assets/1e56bccf-0a3a-4083-b37b-1c80c19956a9)
We Experimented with different parameters that affect the learning process, such as learning rate, the number and size of layers, number of iterations, batch size, epochs.

Architecture 6 provides the best balance of high accuracy, specificity, sensitivity, and precision.

![image](https://github.com/user-attachments/assets/de7f7d2f-ce3c-441f-a8df-7643d1353847)

All classifiers seem to generalize reasonably well to new data. The models are not overfitting, as they perform similarly on unseen test data.

  **Image Data**
  ![image](https://github.com/user-attachments/assets/13708666-4aab-4685-800a-19dd2ab45734)
**The CNN** outperformed all other models with the highest accuracy of **36.78%,** demonstrating its ability to effectively extract spatial features from the image data. Despite its superior performance, there is still room for improvement, particularly in reducing false positive rates for dominant classes like happy. Further optimization, such as deeper architectures or transfer learning, could enhance results.

### File / Folder Structure
- **data**: The dataset are stored in this folder where there are three dataset stored containing excel sheets & images of airline survey.
    - airline_passenger_satisfaction.csv - Contains dataset 1
    - test.csv & train.csv - Contains dataset 2
    - folders train & validate contains image dataset.
    - Models
- **documentation**: The documentation folder contains weekly data.
- **Notebooks**: All working Jupitor notebooks are kept here. These are loaded by individuals with separate trials run during weeks
- **README.md**: Contains details of the project.
