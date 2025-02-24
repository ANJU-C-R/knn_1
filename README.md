
# K-Nearest Neighbors (KNN) Algorithm Implementation for Milk Quality Prediction

## Introduction

Milk is an essential dietary component consumed worldwide, and its quality plays a crucial role in 
ensuring consumer health and satisfaction. The assessment of milk quality traditionally relies on manual 
inspection and laboratory testing, which can be time-consuming and subjective. With advancements in machine 
learning, automated predictive models can be developed to classify milk quality efficiently.

##  K-Nearest Neighbors (KNN) ##
                       
K-Nearest Neighbors (KNN) is a supervised machine learning algorithm used for both classification and regression tasks. 
It is a non-parametric, instance-based algorithm.In classification, KNN assigns a class to a data point based on the majority vote
of its K nearest neighbors. The "distance" between points is typically measured using Euclidean distance, though other metrics like 
Manhattan or Minkowski can be used. The choice of K (number of neighbors) plays a crucial role in model accuracy—too small a K can 
lead to noise sensitivity, while too large a K may smooth out important patterns.

## Dataset Overview

 Dataset is taken from kaggle, which is uploaded as "milknew.csv",link:https://www.kaggle.com/datasets/cpluzshrijayan/milkquality
The dataset used in this study consists of seven independent variables: pH, Temperature, Taste, Odor, Fat, Turbidity,
and Color, which are critical factors in determining milk quality.
 
| **Column Name**   | **Description**                                             
|-------------------|-------------------------------------------------------------
| pH         | Acidity/alkalinity level of the milk                        
| Temperature  | Temperature of the milk in °C                              
| Taste       | Indicates whether the taste is acceptable                    
| Odor        | Indicates whether the odor is normal                        
| Fat         | Indicates whether the fat content is optimal                 
| Turbidity   | Represents the consistency of the milk                       
| Color       | Represents the visual appearance of milk                     
| Grade       | Overall quality classification of the milk                   

The target variable, Grade, categorizes the milk into three quality levels:

**✅Low (Bad)**

**✅Medium (Moderate)**

**✅High (Good)**

## **Step-by-Step Implementation of KNN Algorithm**  

### **1️⃣ Data Loading & Preprocessing**  
- **Reading the dataset** and inspecting its structure.  
- **Checking for missing values**   
- **Encoding categorical variables** 

---

### **2️⃣ Splitting Data into Features & Target Variable**  
- **Defining the feature matrix (x)**, which includes all predictor variables.  
- **Defining the target variable (y)**, which contains the quality of milk

---

### **3️⃣ Splitting Data into Training & Testing Sets**  
- **Dividing the dataset** into **70% training data and 30% testing data** using stratified sampling to ensure an even distribution of classes.  

---

### **4️⃣ Feature Scaling Using Standardization**  
- Since KNN is **distance-based**, different feature scales can negatively impact the model.  
- **StandardScaler** is applied to ensure all features have equal weight in distance computation.  

---

### **5️⃣ Training the KNN Model**  
- **Initializing the KNN classifier** with **k=7**, meaning it considers the 7 nearest neighbors for classification.  
- **Training the model** using the preprocessed training data.  

---

### **6️⃣ Making Predictions on Test Data**  
- The trained KNN model is used to **predict milk quality** on the **test dataset**.  

---

### **7️⃣ Evaluating Model Performance**  

#### **Confusion Matrix Analysis**  
- A **confusion matrix** is generated to visualize the number of **correct and incorrect predictions** made by the model.  
- The confusion matrix provides insights into **true positives, false positives, true negatives, and false negatives**.  

#### **Accuracy Score & Classification Report**  
- The **accuracy score** is computed to evaluate the overall performance of the model.  
- A **classification report** is generated, providing **precision, recall, and F1-score** for each milk quality.  

---

## **Conclusion**  
                                    
This project successfully implements KNN classification to predict milk quality based on the depending features.

