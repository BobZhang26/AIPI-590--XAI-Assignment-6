[![Python Application Test with Github Actions](https://github.com/BobZhang26/Bob_PythonTemplate1/actions/workflows/cicd.yml/badge.svg)](https://github.com/BobZhang26/Bob_PythonTemplate1/actions/workflows/cicd.yml)
## AIPI 590 - XAI | Assignment 6

### Description: 
For a model and dataset of your choice, produce PDP, ICE, and ALE plots. Exploratory analysis of your dataset should be performed to determine the amount of correlation between features. Provide a comprehensive explanation of your plots. Discuss any interesting findings that are shown in the plots. Discuss any differences you see in the PDP and ALE plots. Discuss your exploratory findings around correlation between features and the impact this has (if any) on your results.

### Step 1: Data preperation
The Iris dataset is one of the most famous datasets in machine learning and data science, often used for educational purposes. It consists of data about the physical characteristics of three different species of iris flowers. The Iris dataset is small, easy to understand, and well-suited for demonstrating a variety of machine learning techniques, such as classification, visualization, and dimensionality reduction. It is particularly useful for demonstrating basic machine learning concepts and visualization techniques like scatter plots, decision boundaries, and partial dependence plots.
![image](https://github.com/user-attachments/assets/8c1f3c21-7985-4061-bf51-9b35e2286f71)

![image](https://github.com/user-attachments/assets/f2480fa9-e9da-46c6-a94b-dd6034f44eb8)
### Discussion on correlation:
> The strong correlation between petal length and petal width supports the observation that petal dimensions are the most important features in the model's decision-making process.

> Sepal width and sepal length contribute less to the model's predictions, and their correlations with other features do not significantly affect the results.

> Despite the high correlation between petal length and petal width, both features are useful to the model because they provide slightly different patterns in distinguishing between the species (as seen in the ICE and ALE plots).

Overall, while there are some correlations between the features, the model's performance is not negatively affected because **RandomForest** and other tree-based models can handle correlated features well, often by selecting one over the other during splits.

### Step 2.1: Partial Dependent Plot
![image](https://github.com/user-attachments/assets/29e19e5a-3fc6-4084-91f5-29a864a10474)

### Part 2.2: ICE
![image](https://github.com/user-attachments/assets/f1f81f7a-9c3a-4c8a-ac5f-c4b11594f42d)

### Part 2.3: ALE
![image](https://github.com/user-attachments/assets/93df87bf-d132-468a-b38c-61a106bc6f3c)
![image](https://github.com/user-attachments/assets/0c0fbcf6-49a1-4340-b688-297aebad1e10)

### Part 3: Summary

- **Petal length and petal width** are the most important features for distinguishing between the three Iris species. Setosa has small petal lengths and widths, Versicolor has medium values, and Virginica has large values.
- **Sepal length and sepal width** have less influence overall, though sepal length has a slight impact on differentiating Setosa and Versicolor.
- **Setosa** is easiest to distinguish based on small petal measurements, while **Virginica** can be identified by larger petal measurements. **Versicolor** tends to have medium values for petal dimensions.
These PDPs offer insights into how the RandomForestClassifier uses each feature to classify the flowers, helping us understand which features contribute most to the predictions.
---
1. **Petal length and petal width** are the most important features for distinguishing between the three Iris species. Setosa has the smallest petals (both in length and width), Versicolor has medium-sized petals, and Virginica has the largest petals.
2. **Sepal length** has a moderate impact on the classification, particularly for Setosa and Versicolor, but its effect is less consistent compared to petal features.
3. **Sepal width** has the least impact across all three classes, with the ICE lines being mostly flat for all species.
4. **Variability among instances**: The ICE plots show that the model's predictions can vary significantly for different instances of the same class, especially for features like sepal length and petal width. This variability is captured well by ICE plots and provides insights into how individual samples are affected by each feature.

Overall: The ICE plots confirm that the model relies heavily on **petal features** (length and width) to distinguish between the species in the Iris dataset. The **sepal features** (length and width) play a secondary role, with minimal influence, particularly for Setosa and Virginica.
---
- **Key Features**: The ALE plots for **petal length** and **petal width** show the strongest effects on the model's predictions, which aligns with what is known about the Iris dataset. Virginica has both the longest petals and the widest petals, so the model increases the probability of Virginica as these features increase.
- **Less Important Features**: **Sepal length** and **sepal width** have much weaker effects on the predictions, as their ALE plots are relatively flat or show minimal changes. This indicates that these features are not as critical in distinguishing between the Iris species in the model.

Overall, the **ALE plots** provide a clear picture of which features are most influential in the model's predictions for the Iris dataset, with petal characteristics (length and width) playing the dominant role.



