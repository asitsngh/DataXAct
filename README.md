# DataXAct

## Introduction
This repository was a part of a ML based datathon conducted in my college. I have shared the datasets and problem statement along with my solution. I have also discussed in detail as to what my ideal solution would have been for the following problem.

## Contribution:
I welcome any and all contributions! Here are some ways you can get started:

- Report bugs: If you encounter any bugs, please let us know. Open up an issue and let us know the problem.
- Contribute code: If you are a developer and want to contribute, follow the instructions below to get started!
- Suggestions: If you don't want to code but have some awesome ideas, open up an issue explaining some updates or imporvements you would like to see!
- Documentation: If you see the need for some additional documentation, feel free to add some!

## Proposed solution:
### Preprocessing:
__1. Merge common columns:__
- Merging combines information from multiple datasets into a single dataset.
- Here we can see that our first 3 dataframes, `df1`, `df2` and `df3`, have the same number of rows as each other so they can simply be merged on the basis of indices and saved as a new dataframe, say `df6`.
- However, `df4` and `df5` need to be joined on the basis of the `R13 (MOhms)` and `R14 (MOhms)` column values and saved as a new dataframe, say `df7`.
- `df6` and `df7` can be merged on the basis of common values of the `Flow rate (mL/min)` and `Heater voltage (V)` columns in both the dataframes. The resultant data frame can be saved as a new dataframe, say `df`
- _I found it difficult to find a way to merge `df4` and `df5` and then finally merge the resultant dataframe with `df6` so instead I just directly used `df6` for training purposes._

__2. Drop rows with missing target values:__
- Missing target values hinder accurate analysis or model training.
- Dropping rows with missing target values ensures a clean dataset.
- It guarantees the availability of complete information for model training or analysis.

__3. Use Imputer to Replace Feature Values:__
- Imputation fills in missing values in features or input variables.
- Missing values can occur due to data collection errors or incomplete records.
- Imputation ensures the dataset is complete and usable for model training.
- Common techniques include mean imputation, median imputation, or using advanced methods like regression or machine learning algorithms for prediction.

__4. Splitting of dataset:__
- Split the final dataframe into testing and training data sets using `train_test_split` function from `sklearn` module.

### Model development and selection:
- I tried fitting our training dataset onto 3 different models, namely, linear regression, polynomial regression and random forest regressor.
- Then to test the efficiency of the predictions of these models, I checked and noted the mean squared error values of our output with the target values of the testing dataset.
- This process yielded Random Forest Regressor to be the best of the 3 models.
- The value of the `n_estimators` parameter was inversely proportional to the mean squared error value. However, we needed to ensure that the code didn't take too long to produce the output so we came up with a compromise that ensured the highest possible value of `n_estimators` with a reasonable execution time. That value was 40.
