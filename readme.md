# Prosper Loan Data Exploration
## by Katarzyna Lesiuk


## Dataset

This project explores a dataset containing information regarding 113.937 Prosper Loans listed between 2005-11-09 and 2014-03-10 on Prosper,
i.e. an online peer to peer loan marketplace for borrowers and lenders.
Each row represents one listing and multiple features for each loan are stored in the columns of the data frame (81 for each entry).
The features include numerous borrower characterstics (both quantitative and qualitative in nature), loan features (rate, term, status, amounts related to loan origination and service etc.)
as well as information related to loan investors.

## Summary of Findings

The main point of analysis was to see which features of the loan and the borrower have the greatest impact on loan defaults.
Loans were categorized as performing and nonperforming and a distinction was made for closed and active listings. 
The number of variables was significantly reduced, as analyzing all of the available features was beyond the scope of the project.

A typical Prospect borrower would be someone with relatively short employment history, with annual income between 25-75k USD and a credit rating between B-D.
Approximately 50% of Prosper borrowers were homeowners and most loans had a tenor of 36 months and were used to consolidate existing debt. 

In the analysis the delinquency rate (share of delinquent loans in portfolio) was introduced to show general trends in portfolio performance.
The average historical delinquency rate in the Prosper portfolio is relatively high at 16.7% and even higher for the closed transactions (30.8%).
It was highest for transactions originated between 2006-2007 (almost 40%) and improved significantly starting from 2009 (this is the year when Prosper introduced its own rating system).

Out of the analyzed features the ones that look most promising in terms of their potential to be a predictor of loan delinquency are:
* Loan Term and Listing Category: There are visible differences in performance across different terms and purpose of the loan.
In particular Debt Consolidation & 60m loans tend to have a lower share of delinquent listings compared to other categories.
* Income range - as could be expected the share of performing loans increases with income range.
* Homeowner status - as for the fact of borrower being a homeowner or not the share of delinquent closed loans is slightly lower for homeowners (15%) as compared with non-homewners (18.5%)

Features that do not seem to be significanly impacting debt delinquency:
* Debt to Income Ratio - contrary to my expectations this feature does not seem to impact loan delinquency a lot.
For closed listings the median DIR is slightly lower for performing (0.19) than for nonperforming (0.22) loans.
* Employment status duration - within the active loans categories the performing have a slighly higher median employment status, however the same is not true for the closed categories.
Here the median for both performing and nonperforming loans is almost identical being 53 months for performing and 51 months for nonperforming.

The Borrower rate and Credit Rating both are closely related to loan delinquency and also closely related between each other.
But as the Credti Rating is in fact Prospers prediction of the probability of borrower defaulting on the loan and rates are related to the rating none of these features will be useful for modelling delinquency.

Also based on the conducted analysis it is recommended to limit the loan statused that will be used for modelling to closed deals only,
as the time and tenor analysis of the portfolio shows that using active loans for prediction with most of loans having a tenor of 36m or 60m might lead to misleading results.

## Key Insights for Presentation

For the presenation I will first focus on general delinquency statistics and time trends in the Prosper Portfolio.
Then I will proceed by introducing the bivariate analysis of the main variables of interest chosen for the presentation: Term and Listing Category versus Loan Status variable.
This part will be followed by a multivariate plot showing the relationship between Term / Loan Category and Loan status.



