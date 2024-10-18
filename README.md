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

