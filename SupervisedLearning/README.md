# Machine Learning Project

**Eder Tarifa Fernandez**

## 1. Introduction

This project involves building several supervised learning models using different algorithms and selecting the one that yields the best results, in addition to analyzing all the models created. The dataset used for training and testing the models is focused on classifying different species of mushrooms.

## 2. Problem Description

The selected dataset contains descriptions of 23 species of gilled mushrooms from the Agaricus and Lepiota families. Each species is classified as either definitely edible, definitely poisonous, or of unknown edibility (combined with the poisonous class). Details of how the dataset is structured and the changes made are explained in the file “supervised learning notebook.ypynb.” This file is crucial for understanding the data. Instances with missing values have been removed, and an encoder has been applied to allow the creation of the models.

## 3. Methodology

### K-NN Model

First, a K-NN model was created, applying cross-validation to search for the best value of k between 1 and 70. The best result was obtained using a wide range of k values. Euclidean distance was used to measure the distance between instances, with weights applied to closer neighbors.

* **Error rate vs k for K-NN**  
  (Figure 1: Error rate vs k for K-NN)

### Logistic Regression Model

Next, a logistic regression model was created using different values for the regularization parameter: 0.001, 0.01, 0.1, 1, 10, and 100. The best result was achieved with a regularization parameter of 100, indicating low regularization and allowing the coefficients to fit the training data more freely.

### SVM Model

An SVM model was built with cross-validation to select the best values for C and γ from the following options: 0.001, 0.01, 0.1, 1, 10, and 100. The best model was achieved with C=1 and γ=1. With C=1, the model accepts a certain level of error in the training set to achieve a smoother decision function. A γ value of 1 means the hyperplane fits more strictly to nearby points.

### Decision Tree Model

Finally, a decision tree model was created, again using cross-validation to obtain the best parameters. The key parameters considered were:
- Minimum samples per leaf: 5, 10
- Minimum samples per split: 5, 10, and 20
- Maximum depth: 10, 100
- Criterion: entropy and Gini
- ccp α: 0

The best model split the data based on the gill color of the mushrooms. It divided the dataset into those with gill colors above 3.5 (gray, purple, buff, and green) on one side, and others on the other. The model used features such as bulbous stem shape, surface texture, spore print color, and presence of rings to classify mushrooms as edible or poisonous.

* **Decision Tree Visual Results**  
  (Figure 2: Visual result of decision tree)

## 4. Results

The results from the different models are as follows:

| Model                | Accuracy | Precision | Recall | F1    |
|----------------------|----------|-----------|--------|-------|
| K-NN                 | 1        | 1         | 1      | 1     |
| Logistic Regression  | 0.959    | 0.967     | 0.947  | 0.957 |
| SVM                  | 1        | 1         | 1      | 1     |
| Decision Trees       | 1        | 1         | 1      | 1     |

* **Table 1**: Results obtained from different models

## 5. Discussion

The models created with K-NN, SVM, and decision trees achieved perfect results in the tests using 20% of the data. The logistic regression model performed the worst, and while it might be considered good in other contexts, it is easy to rule it out as the best model since we have three other models with superior performance.

Among the three models with perfect results, the decision tree is the most interpretable. This model provides insight into how decisions are made based on different features of the mushrooms, making it valuable for understanding the model’s reasoning.

## 6. Conclusion

In conclusion, the decision tree model was chosen. While K-NN, SVM, and decision trees all performed excellently, the decision tree offers the advantage of interpretability, which can be crucial when explaining how the model arrived at a particular conclusion.

## 7. References

- Database: [UCI Mushroom Dataset](http://archive.ics.uci.edu/dataset/73/mushroom)
