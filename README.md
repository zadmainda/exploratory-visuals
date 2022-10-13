# exploratory-visuals

# (Investigating the Relationships between Variables in the Prosper Loan Data)
## by (Zadock Mainda)


## Dataset - Prosper Loan Data

> The Prosper Loan Data contains a wide range of information that not only describes the borrowers'  General details and loan specifics but also Estimated yield among many others. These details are spread over 81 separate columns for the 113,937 loans taken at the credit facility between Nov 2005 and Mar 2014. Even though most of these variables apply to all loans between 2005 and 2014, there are some that applicable to certain period only. For instance, The prosperScore and ProsperRating are assigned to loan listings that were created after July 2009. 

> Before investigating the relationships between the dataset's variables, I selected a small subset of variables that I will use to answer my questions. After that, I proceeded with both visual and programmatic assessment of the dataset. I noted down some of the issues before I cleaned and rectified to fit my objectives.

##### Definition of the variables chosen for analysis
1. ListingKey - Uiinque Key fo each loan
2. ListingCreationDate - date the listing was created
3. CreditGrade - the credit grading assigned to Borrower at time of loan listing
4. LoanStatus - current status of the Loan
5. BorrowerRate - Interest Rate for the Loan
6. ProsperScore - Custom credit score assigned to borrower for loans taken after July 2009 
7. EmploymentStatus - Employment status of borrower at time of loan application
8. EmploymentStatusDuration - The length of emloyment period in months
9. IsBorrowerHomeowner - True or false. Depends on whether borrower had active mortgage payments
9. MonthlyLoanPayment - Amount required to be paid at the end of the month
10. PublicRecordsLast10Years - Number of public records  
11. DebtToIncomeRatio - debt to income ratio at time of loan listing
12. IncomeRange - borrower's income range at time of loan listing
13. LoanOriginalAmount - The initial loan amount given to borrower

##### Quality Issues
1. ListingCreationDate is a string
2. Duplicate descriptor in the Employment status ('Employed' & 'Full-time' )
3. IncomeRange is a string instead of Categorical datatype
4. CreditGrade is a String object


## Summary of Findings

Most of the borrowers in this dataset have a C credit rating. The next credit rating with the most borrowers is D with a total of 5,153 people. From the visualization we can also see that the least amount of loans went to borrowers with a NC (No Credit) rating. Only 141 people with No Credit were given loans.

The most common employment status listed by loan borrowers was "Employed" at 93677. The least common employment status listed was "Retired" with a meagre 795 loans. Home Ownership rates between the Employed Categories and all other categories vary greatly. Home ownership is highest amongst the Employed and lowest among the Retired category.

From our listCreationDate Barchart, the highest number of loans were listed in Jan while the least number of loans was listed in April. There is a continuous downward trend from Jan that ended in April. And then from April We have a clear upwards trend for the second quarter upto July before the number of dips slightly before picking another upwards trend until the last month.

There is a weak but positive relationship between the DebtToIncomeRatio and BorrowerRate variables. As the BorrowerRate increases, DebtToIncomeRatio tends to increase also.

There was significant positive relationship between the Loanamount and the borrowerRate in the top most rated credit ratings ('AA', 'A', 'B', 'C', 'D'). This means that the borrowing rate increased as the loan amount increased in each credit category. There was also slightly strong positive relationship between loanamount and Borrowerate in the last 2 credit ratings ('E', 'HR'), but it was a positive relationship nevertheless. This somehow negates our previous findings where we saw when the Original Loan Amount increased, the borrowing rate decreased.

As the BorrowerRate increases, DebtToIncomeRatio tends to increase also for both home owners and non-homeowners. The relationship was more pronounced in homeowners category which had a bigger correlation coefficient than that of the non-homeowners. This virtually reasonates with our earlier findings where we found that the DebtToIncomeRatio and BorrowerRate variables had a positive relationship.

For the borrowers who listed their income as $0, the count of people increased as the crediting rating reduced. When we examined the highest income group , most of the borrowers have the best AA credit rating, while the worst credit rating has the least count of borrowers.


## Key Insights for Presentation


> Most of the borrowers in this dataset have a C level credit rating. This is crucial information to assist stakeholder's pinpoint the credit garde of the most borrowers and perhaps commission further exploration into their loan repayment rates. 

> The highest number of loans were taken in Jan while the least number of loans was listed in April. Understanding borrowing patterns throghout the year can assist the credit facility prepare incentives in advance to attracts borrowers in low seasons.   

> There is a weak but positive relationship between the DebtToIncomeRatio and BorrowerRate variables. As the BorrowerRate increases, DebtToIncomeRatio tends to increase also.