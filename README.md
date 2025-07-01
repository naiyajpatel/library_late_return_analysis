# library_late_return_analysis

Project Overview:

This project analyzes library data, checkout data, customers data and books data to identify patterns in late book returns and builds a logistic regression model to predict the likelihood of a late return. The goal is to provide actionable insights to help libraries reduce late returns and improve circulation efficiency.


Problem Statement: 

Late book returns create bottlenecks in circulation, reduce book availability, and incur late fees. Using borrower, book, and checkout data to check the pattern in late returns and predict which books are likely to be returned late via Logistic regression.  


Steps performed from start to end in the project:

1. Importing csv files
2. Performing Exploratory Data Analysis
3. Data Cleaning and Manipulating
4. Multivariate Analysis by joining the dataset
5. Prediction Analysis by Logistic Regression Model building
6. Train and Test Split/ verifying performances of model
7. Odds Ratio
8. Insights and Recommendations
9. Explanation: How to present them to get buy-in?


Modeling Approach:

1. Model used: Logistic Regression
2. Techniques: Combined 4 CSVs using joins
3. Feature engineering
4. Used class_weight='balanced' to handle class imbalance
5. Metrics evaluated: Accuracy, Precision, Recall, F1-score, Confusion Matrix, ROC-AUC Curve
6. Odds Ratios for feature interpretability


Images: 

![late_return_by_title](https://github.com/user-attachments/assets/18baf4bd-d395-466f-a104-28ba103ecfcf) - Highest late returns based on book title

![late_return_by_pages](https://github.com/user-attachments/assets/bcca70d9-ae05-40cf-baa0-6f51dd61d6e8) - Highest late returns based on pages of book

![late_return_by_price](https://github.com/user-attachments/assets/b89bf903-1f8e-41be-94f9-0ebec3e4bd7b) - Highest late returns based on price of the book

![late_return_by_authors](https://github.com/user-attachments/assets/4f892b9b-f22b-4fdc-857d-5bd8d91ff11a) - Highest late returns based on authors of the book

![late_return_by_categories](https://github.com/user-attachments/assets/5ef8bc56-d49a-4522-88f6-cfc9b9a2a8e9) - highest late returns on categories of the book

![late_return_by_gender](https://github.com/user-attachments/assets/5925959c-f9c4-4fae-9127-ac56c5c793c9) - highest late returns based on gender of customers

![late_return_by_education](https://github.com/user-attachments/assets/afd3f297-d947-4804-85bf-c19f501cc4a6) - highest late returns based on education of the customers

![late_return_by_occupation](https://github.com/user-attachments/assets/7521da99-84d6-4a3b-b98d-faf9c2e96367) - highest lata returns based on occupation of the customer

![late_return_by_age_group](https://github.com/user-attachments/assets/84e1d66f-4ca3-4dc1-bc75-64911c40e97f) - highest late returns based on age group of the customer

![Late_return_by_checkout_month](https://github.com/user-attachments/assets/d75b2079-a6cd-4bfb-bb7e-c85b2ef9331c) - highest late returns based on checkout month

![confusion_matrix_train](https://github.com/user-attachments/assets/96db3fb2-2fbb-4e13-a473-fdf658bf3901) - confusion matrix of Log Reg model of train and test set

![ROC_curve_test](https://github.com/user-attachments/assets/c9d6f486-beb4-4274-9f81-6ba451d782fc) - ROC curve of test model



Key Insights:

1. Late returns peak in April, August and December — likely due to exams, holidays, and branch closures.
2. Branch at 205 NE Russell St has the highest late-return rate (13.04%).
3. Age 51–65, male customers, and those in Business & Finance occupations are more prone to return books late.
4. Books priced > $400, with >1100 pages, or in Agriculture categories show higher late return rates.
5. Missing education information also correlates with higher late return likelihood.
6. Certain authors (e.g., Khan & Jain) and book titles are disproportionately late.

Recommendations:

1. Enable auto-renewals before peak late months (April, August & December)
2. Install fast-drop return bins at high-risk branches (e.g., 205 NE Russell St)
3. Send tailored reminders (email/SMS/push notifications) to high-risk users (e.g., age 51–65, Business/Finance occupations)
4. Shorten loan periods or require deposits for expensive or long books
5. Tag high-risk books (based on author/category) for shorter checkout duration or limit renewals
6. Embed model in the library system to flag high-risk checkouts in real time
7. Improve data collection, especially for missing user attributes (e.g., education)

Next steps: 

Due to very poor model built due to imbalanced class weights, we will ask for initiating pilot project at high risk late return branch of library (205 NE Russell St, Portland, Oregon) where we can collect more data and build stronger model to predict late returns which can help staff to take action on possible late returns before time
