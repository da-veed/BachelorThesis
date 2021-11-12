# Introduction
This repository holds data and code for my Bachelor thesis: *"Exploring machine learning models for churn prediction of membership subscriptions"*. 

Huge thank you to [Moji Ajele](https://www.linkedin.com/in/mojiajele) and [BNI Alberta South](https://bnisalberta.ca) for making my thesis possible. Highly recommend for anyone who owns a small/medium business to look into BNI as a networking and advertising opportunity.

# Project objective
Devise a ML model for for predicting who won't be renewing their membership with a precision acceptance score of at least 80% (the performance metric and threshold might be re-evaluated after performing some EDA on the data and determining class balance).

**Extra:** If a probability model meets the performance criteria mentioned above then determine users who are within 30% - 60% chance of renewing. Those users have the biggest potential to be converted from non-renewals to renewals.

# Data
- The model will be based on PALMS data which was shared with me by BNI Alberta South. BNI creates local groups of entrepreneurs who form relationships and refer eachother's businesses
- BNI business model: yearly membership subscription
- The data isn't disclosed in this repository due to an agreement on preserving BNI members' privacy.
- All data has been anonymized

## Datasets: PALMS
- Data from 2015-01 to 2021-10 in a monthly format (82 .csv files)
- Each months PALMS data contains information about member performance

Here are a couple of links with a legend/explanation of the PALMS data: [Link 1](https://support.bniconnect.com/hc/en-us/articles/219067027-Summary-PALMS-Report) and [Link 2](https://bniblog.co.nz/bni-core-values/accountability/palms-for-beginners/).


## Dataset: database_data
General information about all members. Specifically useful information here are: member drop date, member renewal date.

## Dataset: dropped_members
Contains information when a given member was dropped from the system (his subscription was cancelled).


# Project plan
1. [x] 1. Prepare for thesis
   1. [x] Get data
   2. [x] Business objective
   3. [x] Create a cleaning log
   4. [x] Decide on metric and threshold of choice
2. [ ] 2. Prepare & clean data (*"cleaning_log.md"*)
   1. [x] Anonymize data
   2. [x] Check control sums to ensure PALMS data hasn't been duplicated
   3. [x] Concatenate PALMS data
   4. [x] Create a master dataset - merge
   5. [x] Ensure data integrity:
      1. [x] Fix member records with two or less months with negative year of membership
      2. [x] Fix member records with more than two months with negative year of membership
      3. [x] Remove duplicate records
   6. [ ] Aggregate 9-month data
   7. [ ] Re-merge data which wasn't supposed to be aggregated
   8. [ ] Label: renewing/not renewing
3. [ ] 3. Exploratory Data Analysis
   1. [ ] Feature engineering:
      1. [ ] Seat popularity rate
      2. [ ] Chapter retention rate
      3. [ ] Chapter size
   2. [ ] Feature selection
   3. [ ] Analyze:
      1. [ ] Summary Statistics
      2. [ ] Outliers
      3. [ ] Normality
      4. [ ] Visual representations
   4. [ ] Scale
   5. [ ] [Extra] Perform data Analysis:
      1. [ ] Which features are the most indicative if the member will or won't renew?
      2. [ ] Which seats are the most profitable?
      3. [ ] How does membership length affect renewal probability?
4. [ ] 4. Create ML models
   1. [ ] Split data: train, validate, test
   2. [ ] Hyperparameter tuning (cross-validate & plot)
   3. [ ] Learning curve
   4. [ ] Power analysis
   5. [ ] Test results
5. [ ] 5. Meet with promotor to discuss results and get feedback
6. [ ] 6. Write LaTeX thesis 
