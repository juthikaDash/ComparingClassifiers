# ComparingClassifiers
In this practical application assignment, my goal is to compare the performance of the classifiers such as:
  * k-nearest neighbors(KNN)
  * Logistic Regression(LR)
  * Decision Trees(DT) 
  * Support Vector Machines(SVM)
on Bank marketing data

## Dataset: 
The data is from a Portuguese banking institution and is a collection of the results of multiple marketing campaigns. The classification goal is to predict if the client will subscribe to a term deposit (variable y). There are 16 features and 45211 rows of data.
The dataset is available here: https://archive.ics.uci.edu/dataset/222/bank+marketing

### Business Objective:  

The business objective consists of leveraging the dataset supplied by a Portuguese bank regarding past direct marketing campaigns. Using this dataset of 17 campaigns and over 79,354 contacts, our goal is to create a model capable of predicting the success of a marketing campaign. Success in this case is defined as the number of people accepting to purchase the product (a long-term deposit with good interest rates).  

To do so, we will compare the classification methods of:  
* K-nearest neighbors (KNN)
* Logistic Regression (LR)
* Decision Trees (DT)
* Support Vector Machines (SVM)


### Scoring:

Before beginning our exploration of various models, it is important to define the criteria we will monitor and compare for our conclusion. To do so, we will explore the various scoring track during our exploration.  

As referred to in the paper 'Using Data Mining for Bank Direct Marketing: An Application of the CRISP-DM Methodology' by Moro, S. & Laureano, M.S. The AUC_ROC offers a great way to track the performance of our model in our business context. The AUC plots the False Positive Rate (FPR) versus the True Positive Rate (TPR). This measure will allow us to track the number of clients the model miss misidentified as purchasers of the product (false positive) while maximizing the real buyers of the product. In the business context, such an approach makes sense as you are looking to limit the resources spent on non-buyers hence you are hoping to have a low FPR to maximize your campaign's profitability.  

In addition, we will track the Accuracy, F1, Precision, and Recall to better understand the overall performance of each model. To understand the cost behind each model, we will also collect the run time of each model to better track the tradeoff of accuracy vs time.


### Summary of Findings
Based on the search results provided, here is a summary of the key findings regarding the business objective of creating a model to predict the success of marketing campaigns for a Portuguese bank:
* The dataset consists of 17 past direct marketing campaigns and over 79,354 contacts, with the goal of predicting whether a customer will accept a long-term deposit product.
* The analysis will compare the performance of four classification methods: K-Nearest Neighbors (KNN), Logistic Regression (LR), Decision Trees (DT), and Support Vector Machines (SVM).
* The primary evaluation metric will be the Area Under the Curve of the Receiver Operating Characteristic (AUC-ROC), which measures the trade-off between the True Positive Rate and False Positive Rate. * This is an appropriate metric given the business objective of maximizing successful contacts while minimizing wasted resources on non-buyers.
* Additional metrics like Accuracy, F1-score, Precision, and Recall will also be tracked to provide a more comprehensive understanding of the models' performance.
* The dataset is class-imbalanced, with approximately 89% "no" and 11% "yes" responses. This will need to be considered when building and evaluating the models.
Based on the results, the Logistic Regression model performed the best.
* Further exploration could include optimizing the hyperparameters of the top-performing models, addressing the class imbalance, incorporating additional features, and handling missing data.

In conclusion, the Logistic Regression model appears to be the most suitable choice for predicting the success of the bank's marketing campaigns, based on the information provided in the search results. However, additional refinements and experimentation may be necessary to improve the model's performance further.

### Exploring Model improvement:
Based on the experiment and research provided, there are several ways to further improve the machine-learning model for this problem:
* Explore parameters for top models:
  The search results indicate that the top-performing models were logistic regression and decision trees. To further improve these models, you could:
  *  For logistic regression, experiment with different regularization techniques (L1, L2, elastic net) and tune the regularization strength to address any overfitting.
  *  For decision trees, try adjusting the maximum depth, minimum samples per leaf, and other hyperparameters to find the optimal model complexity.

* Address Class imbalance:
  The search results suggest the dataset has an imbalanced target variable, with some outcomes being more prevalent than others. To mitigate this issue, you could try:
  * Oversampling the minority class using techniques like SMOTE.
  * Undersampling the majority class to balance the dataset.
     Applying class weights during model training to give more importance to the minority class.
  
* Incorporate additional features
  The search results mention several additional features that could be incorporated to improve model performance, such as:
   * Macroeconomic indicators
   * Temporal features like month and day
   * Handling unknown/missing values in the existing features
  
