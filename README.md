
# (Dataset Exploration Title)ProsperLoan Data Exploration
## by Andrei Tibuliac


## Dataset

This project is part of the Udacity Data Analyst Nano Degree Program. I conducted an exploratory data analysis on a data set from Prosper, which is America’s first marketplace lending platform, with over $9 billion in funded loans. This data set contains 113,937 loans with 81 variables on each loan,  including loan amount, borrower rate (or interest rate), current loan  status, borrower income, borrower employment status, borrower credit  history, and the latest payment information.

The main purposes of this project are to summarize the characteristics of  variables that can affect the loan status and to get some ideas about the  relationships among multiple variables using summary statistics and data  visualizations.
The dataset can be found in the repository for R's ggplot2 library [here](https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv.)

## Summary of Findings

The StatedMonthlyIncome is highly right skewed.I remove loans with missing borrowerAPR and BorrowerRate information and removed columns and columns that are not really useful in the dataset. From the number of listings in each BorrowerState I can see that the state with most number of borrowers significantly more than other states was CA (California). I think a significant number o clients refuse to share the real information about the Occupation status so a number of clients where were passed with the status 'Other'
We can see that most of the clients where reluctant to offer their real occupation status so the first two professions are of 'others' and 'professions' category which it doesn't necessarily help us to much to determined their real jobs. 
Borrowers with different letter ratings were also analyzed. It came out that borrowers with the lowerest rating(HR) received higher APR percentage, and borrower with high rating A(A) received lowers APR percentage. This differentiate groups of people in terms of APR received based on their rating and scores.
The final structure after cleaning,because some of the information where not useful for my exploring , of the dataset is of with 113912 informations about the loans , with 72 features . Most variables are numeric in nature, but there are some that are categorical, like 'LoanStatus','IsBorrowerHomeowner', 'IncomeVerifiable', etc.The huge dataset with a lot of informaton allowed me to have deeper look at the question what factors affect a loan’s outcome status.
This exploring investigation might help the Prosper company to minimize the default risk and and to set the right interest rate and to find out what factors predict the outcome of a loan best.


## Key Insights for Presentation

First, histogram plot were created to visualize the distribution on borrower's APR and Rate percentage. After exploring all possible variables related to BorrowerAPR and BorrowerRate. EstimatedReturn and  AvailableBankcardCredit  has the strongest relationship with Borrower's APR . Pairgrid plot and Heatmap were also created to find out the correlation between CurrentCreditLines, OpenRevolvingAccounts,AvailableBankcardCredit,LoanMonthsSinceOrigination and MonthlyLoanPayment.
I studied the relationships between IncomeRange and ProsperRating and found the that clients with the best ratings are those that have higher salaries.
When a borrower has relatively low credit amount, under 20,000, the probabilities of getting low and high interest rates are similar.Nevertheless, when the borrower’s credit amount is high , above 50,000, is more likely to get a lower interest rate.
I do observe that the relationships between CurrentCreditLines and OpenCreditLines are quite based on the loan status are quite similar.
Prosper Loan Company does a good job in collecting their loan data of clients. However, It takes some steps in cleaning and simplifying the dataset before it ready to be used. I think the company can have a good and detailed understanding of their clients as well as they can create a plan to better their products/services. Monthly homeowners pay of the who own a home and those who don't own a home overlap between 2011 and 2012, meaning they are paying an equal amount of money. There is a fall between Q2 of 2008 and end of 2010, which can be related to the global financial crisis. I also found that the company may implemented some changes to its business model between 2009 and 2010 . Therefore, an analysis of loans created before that date only has limited meaning if you want to draw conclusions about company as it operates today.
I could further detect the following relationsship between Loan status, Prosper Score and interest rate: the higher the Prosper Score, the lower the interest rate, the lower the risk for Prosper that the loan will be defaulted, charged-off or has past due payments. So, borrower with a higher Prosper Score get a lower interest rate due to the lower risk that the loan will be defaulted.
