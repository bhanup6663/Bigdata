# G26: Fraud Analysis for Vehicle Insurance Claim

There are several insurance-claim frauds being faced by the insurers. It has become quite frequent over the years. These frauds have major repercussions such as higher premiums for honest policy holders, more scrutiny while issuing policy etc. There are several acknowledged types of frauds including but not limited to identity fraud, staged accidents and inflated claims. In a recent research, it was claimed that insurance fraud grows 23% YoY and has a global impact of $6.4 billion. Hence, in order to solve this problem, several fraud detection techniques can be applied through ML algorithms where the goal is to identify patterns and anomalies as quickly and efficiently as possible that could indicate fraudulent claims. This will help the insurance companies to reduce their losses as well as increase people’s trust in the insurance industries.

For vehicle insurance claim fraud, a dataset is chosen from Kaggle having 33 features and 15420 data entries. This dataset has several features that indicate the following:
Vehicle: make, category, price, age
Customer:  sex, age, marital-status, driver-rating, number-of-vehicles
Policy: policy-number, fault, type, deductible, days between events, police-report filed, witness present, agent-type, accident-area, address-change, base-policy, supplements
Data labeled with binary classification if fraud found (0 or 1)

The data size available for this use-case is sufficient - more than 10 times degrees of freedom. The other observations ensure acceptable nulls/missing values (2%), the data is unbalanced 6%, however, it is in line with insurance industry trends.

The following research questions may be addressed from the analysis:
Can insurance claim fraud be predicted and what is the performance of the algorithms?
Which features are important and will affect predicting the fraud?
What is the importance of claim data completeness in fraud detection?

This is a supervised ML (classification) problem. Considering the numerical and categorical data in the dataset, the algorithms that could be used are decision-trees, random-forest and logistic regression. The dataset will be undersampled and split into training, validation and test. To account for undersampling in the dataset, stratified k-fold cross validation shall be applied. Decision trees can also be used for feature selection along with Pearson (or Kendall) correlation. While decision trees perform better with categorical data, logistic regression could perform better given that the size of data is less.

The primary KPI for this analysis shall be precision, recall and F1 score over accuracy since it’s more important to predict fraudsters.
