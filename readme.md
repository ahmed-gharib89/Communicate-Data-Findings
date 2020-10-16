# Prosper Loan Exploration
## by Ahmed Gharib

## Introduction
#### About Prosper

From the [Prosper](https://www.prosper.com/) website. Prosper was founded in 2005 as the first peer-to-peer lending marketplace in the United States. Since then, Prosper has facilitated more than $17 billion in loans to more than 1,030,000 people.

Through Prosper, people can invest in each other in a way that is financially and socially rewarding. Borrowers apply online for a fixed-rate, fixed-term loan between \\$2,000 and \\$40,000. Individuals and institutions can invest in the loans and earn attractive returns. Prosper handles all loan servicing on behalf of the matched borrowers and investors.

Prosper Marketplace is backed by leading investors including Sequoia Capital, Francisco Partners, Institutional Venture Partners, and Credit Suisse NEXT Fund.
## Dataset

[Prosper Loan Dataset](https://www.google.com/url?q=https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv&sa=D&ust=1602316069250000&usg=AOvVaw3v_Fjzy60OI_JxN1zu63ds) (Last update 03/11/2014)

- This dataset contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others.

- [This data dictionary](https://www.google.com/url?q=https://docs.google.com/spreadsheet/ccc?key%3D0AllIqIyvWZdadDd5NTlqZ1pBMHlsUjdrOTZHaVBuSlE%26usp%3Dsharing&sa=D&ust=1602316069252000&usg=AOvVaw30T5Cb1SJcH_-mM-PE6sWH) explains the variables in the data set.


## Summary of Findings

- The distribution of `BorrowerAPR` is approximatly normal with a mean of 22.26%, median of 21.47%, minmun rate of 0.65% and maximum of 51.23%. and most of the values ranges between 10% and 45%.
- The prosper rating and score distribution is normal, most term used is 36 Months and most of the individuals income range falls between 25,000 and 75,000.
- The top reason for prosper loans is debt consilidation and there is a lot of people didn't reveal for the reason by chosing nothing.
- Most of the Borrower was from California followed by Florida and Texas.
- Employment Status Duration has a long-tailed distribution with a lot of emplyees between $0 \to 100$ months in their current position<br> when plotted the log-scale, the distribution is roughly normal with a peak around $80 \to 90$ months.
- Loan delinquent days most users pay on time with most of them with 0 delayed days then from $1 \to 300$ is roughly uniform with a peck around 120 days or 4 months and few delayed more than a year and we will go deeper into this and see that those for defaulted loans.
- There is a postive relatioship between `ProsperScore` , `AvgCreditScore` and `LoanOriginalAmount`.
- There is a negative relationship between `BorrowerAPR` and those 3 variables (`ProsperScore` , `AvgCreditScore` and `LoanOriginalAmount`).
- there is no clear relation between `BorrowerAPR` and the payment `Term`.
- the lowest median for `BorrowerAPR` is for Completed followed by Current `LoanStatus`.
- the negative relation between `BorrowerAPR` and `ProsperScore` is appearing here again.
- there is a relation between `BorrowerAPR` and `EmploymentStatus` as it tends to be lower for emplyed individuals than not employed with some cosiderations for retired and part time jobs to be the lowest.
- the `BorrowerAPR` tend to be lower for Homeowners than if the individual doesn't own a house.
- again we see that the `BorrowerAPR` tend to be high for not emploed individuals in `IncomeRange` with some considerations for people with 0 income.
- and for the other relation between `BorrowerAPR` and `ListingCategory` some reasons tend to get lower rate than others but we will dig more in multivariate exploration to see if this effect because of the `ListingCategory` or there is another correlated variable that make this effect.
- and about the relation between `BorrowerAPR` and the `BorrowerState` and `Occupation` are not clear.
- 0 Not displayed `IncomeRange` for current loans which means that the policy of the website changed lately.
- Most of Defaulted loans were for individuals who didn't displayed their income.
- `LoanOriginalAmount`, `ProsperScore` and `AvgCreditScore` are the most features that affect the `BorrowerAPR` as the larger they are the lower the interest rate is.
- `LoanStatus` is effected the most by `IncomeRange` and `EmploymentStatus` as most of defaulted loans are for people who were unemployed. 
- `AvgCreditScore` and `LoanOriginalAmount` is positively correlated we can expect that the higher score the higher the loan amount the individual can borrow.
- The highest total `LoanOriginalAmount` was for individuals who are located in California state.
- Not employed idividuals have the highest APR for current loans suggesting that now Prosper company consider them the highest risk and the lowest rate for employed individuals.
## Key Insights for Presentation

In this investigation I wanted to look at what affects the Borrower APR and how other features affect the loan status.
