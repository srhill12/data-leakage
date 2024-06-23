# Spotting Data Leakage

## Purpose

Examine two datasets and attempt to find the column that is leaking data into the model. 

### Part 1: Crowdfunding

1. Import and split the data, train a model, and calculate the training and testing scores. 

2. Display the head of the DataFrame and examine each column. 

3. Check the correlation of the columns against the outcome column.

4. Plot the rewards_given and outcome columns in a scatter plot.

### Part 2: Start Up Success

1. Import and split the data, train a model, and calculate the training and testing scores.

2. Display the head of the DataFrame and examine each column. Do you see any columns that might provide information that would not be available when trying to predict whether a crowdfunding project would reach its goal?

3. Check the correlation of the columns to the Firm Category column.

4. Plot Firm ID and Firm Category in a scatter plot.

## Conclusion

The second plot, which plots Firm ID against Firm Category, suggests that data leakage may be present. This is because the Firm ID is likely a unique identifier that directly correlates with the Firm Category, thus revealing the target variable (Firm Category) in a manner that should not be used for training a model. Using identifiers that are not generalizable features can lead to overfitting and poor performance on unseen data, which is a classic symptom of data leakage.
