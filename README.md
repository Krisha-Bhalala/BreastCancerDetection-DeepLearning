# Breast Cancer Detection Using Deep Learning

## Table of Contents
- Introduction
- Data Loading and Preprocessing
- Neural Network Design and Training
- Performance Evaluation
- Comparison with Other Methods
- Conclusion
- Dataset Citation
- How to Run the Project

## Introduction
Breast cancer is one of the most common types of cancer, and finding it early is very important for better treatment. This project uses a method called deep learning to look at data from the Wisconsin Diagnostic Breast Cancer (WDBC) dataset. The goal is to tell whether a tumor is benign (not cancerous) or malignant (cancerous). The dataset has **569 samples** and **30 features** that describe different characteristics of breast cells.

## Data Loading and Preprocessing
We start by loading the WDBC dataset from a public source. We clean the data by removing unnecessary columns and changing the diagnosis into two categories: benign or malignant. We also make sure all features are on the same scale so that our model works better.

### Steps:
1. Remove the unnecessary ID column.
2. Change the diagnosis column to show "benign" or "malignant."
3. Scale the features so they are all between 0 and 1.

## Neural Network Design and Training
We create a simple neural network with the following structure:

- **Input Layer:** 30 nodes, one for each feature.
- **Hidden Layers:** Two layers, one with 16 nodes and another with 8 nodes.
- **Output Layer:** One node that gives a probability (between 0 and 1) of whether the tumor is malignant.

We train this model using a specific package in R, stopping early if the error does not improve.

## Performance Evaluation
After training our model, we test it on a separate set of data and create a confusion matrix to see how well it performs. We look at several metrics, including accuracy (how often it’s correct), sensitivity (how well it finds cancer), specificity (how well it identifies non-cancer), precision, and Kappa score.

## Comparison with Other Methods
Along with our neural network, we also use a Random Forest classifier to see how it compares. This model uses **500 decision trees** to make predictions, and we evaluate its performance in the same way as the neural network.

## Conclusion
This project shows that machine learning can help in detecting breast cancer. While our neural network did not perform very well, the Random Forest model showed high accuracy and reliable results. Therefore, we recommend using the Random Forest classifier for this task because it performed better.

## Dataset Citation
Wisconsin Diagnostic Breast Cancer (WDBC) dataset. (1995). UCI Machine Learning Repository. Retrieved from UCI Repository.

## How to Run the Project

To run this project, follow these steps:

1. **Install R and RStudio:**
   - Download and install R from [CRAN](https://cran.r-project.org/).
   - Download and install RStudio from [RStudio's website](https://www.rstudio.com/products/rstudio/download/).

2. **Install Required Packages:**
   - Open RStudio and run the following commands in the console to install necessary packages:
     ```
     install.packages("neuralnet")
     install.packages("randomForest")
     install.packages("caret")
     ```

3. **Open the R Markdown File:**
   - Locate the uploaded `.Rmd` file in your project directory.
   - Open it in RStudio.

4. **Run the Code:**
   - Click on the "Knit" button in RStudio to generate an HTML report from your `.Rmd` file.
   - Alternatively, you can run each code chunk individually by clicking on "Run" while selecting each chunk.

5. **View Results:**
   - After knitting or running the code, you will see an HTML file generated that contains all your results and visualizations.

By following these steps, you can successfully run this project and explore breast cancer detection using deep learning.
