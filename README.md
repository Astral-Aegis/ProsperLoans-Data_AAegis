# ProsperLoans-Data_AAegis
Udacity ProsperLoans Project by Aibangbee Darlington

## Dataset

The Prosper Loans data set contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others.

 This dataset is analysed to answer questions like:
* What factors affect a loan’s outcome status?
* What affects the borrower’s APR or interest rate?
* Are there differences between loans depending on how large the original loan amount was?
* Some of the important features considered in this analysis are defined and explained below. For a full definition of all the features contained in this dataset, this [data dictionary](https://www.google.com/url?q=https://docs.google.com/spreadsheet/ccc?key%3D0AllIqIyvWZdadDd5NTlqZ1pBMHlsUjdrOTZHaVBuSlE%26usp%3Dsharing&sa=D&source=editors&ust=1671037491835352&usg=AOvVaw1iRZ11ayBTHS1WDx0Ky7sR) explains the variables in the data set.


* The ProsperLoans Dataset contains 113937 loan entries under grouped under 81 features(columns) some of which are very important factors that affect or explains the circumstances surrounding a loan issue or status. These features contains information on things like: 
* Loan Type, Amount, Date, Interest Rate
* Borrower financial information: Occupation, Employment Status, Credit score, income range
* Loan information: Status


Some of the key Columns or Features that could potentially answer some key questions on visualisation are:

   **Variable       :         Description**
* **Term:**	The length of the loan expressed in months.
* **LoanStatus:**	The current status of the loan: Cancelled, Chargedoff, Completed, Current, Defaulted, FinalPaymentInProgress, PastDue. The PastDue status will be accompanied by a delinquency bucket.
* **ClosedDate:**	Closed date is applicable for Cancelled, Completed, Chargedoff and Defaulted loan statuses.
* **BorrowerAPR:**	The Borrower's Annual Percentage Rate (APR) for the loan.
* **BorrowerRate:**	The Borrower's interest rate for this loan.
* **LenderYield:**	The Lender yield on the loan. Lender yield is equal to the interest rate on the loan less the servicing fee.
* **ProsperRating (Alpha):**	The Prosper Rating assigned at the time the listing was created between AA - HR. Applicable for loans originated after July 2009.
* **ProsperScore:**	A custom risk score built using historical Prosper data. The score ranges from 1-10, with 10 being the best, or lowest risk score. Applicable for loans originated after July 2009.
* **ListingCategory:**	The category of the listing that the borrower selected when posting their listing: 0 - Not Available, 1 - Debt Consolidation, 2 - Home Improvement, 3 - Business, 4 - Personal Loan, 5 - Student Use, 6 - Auto, 7- Other, 8 - Baby&Adoption, 9 - Boat, 10 - Cosmetic Procedure, 11 - Engagement Ring, 12 - Green Loans, 13 - Household Expenses, 14 - Large Purchases, 15 - Medical/Dental, 16 - Motorcycle, 17 - RV, 18 - Taxes, 19 - Vacation, 20 - Wedding Loans
* **BorrowerState:**	The two letter abbreviation of the state of the address of the borrower at the time the Listing was created.
* **Occupation:**	The Occupation selected by the Borrower at the time they created the listing.
* **EmploymentStatus:**	The employment status of the borrower at the time they posted the listing.
* **EmploymentStatusDuration:**	The length in months of the employment status at the time the listing was created.
* **IsBorrowerHomeowner:**	A Borrower will be classified as a homowner if they have a mortgage on their credit profile or provide documentation confirming they are a homeowner.
* **CreditScoreRangeLower:**	The lower value representing the range of the borrower's credit score as provided by a consumer credit rating agency.
* **CreditScoreRangeUpper:**	The upper value representing the range of the borrower's credit score as provided by a consumer credit

## Main feature(s) of interest in your dataset?

#### The main features of Interest in my DataSet are:
* BorrowerRate(interest Rate on loans), BorrowerAPR(annual interest on loans), LoanStatus(outcome on the loan), Type of Loans(ListingCategory)

## Features in the dataset that will most likely help support the investigation into feature(s) of interest?

#### Some features in the dataset that may help in my investigation are features like:
* The borrowers financial information features like: Occupation, EmploymentStatus, CreditScoreRange, CurrentCreditLines BorrowerRAte, DebtToIncomeRatio, IncomeRange, StatedMonthly income!
* The Loan features like: amount, Term, BorrowerAPR, BorrowerRAte, ProsperRating, LenderYield, EstimatedEffectiveYield


## Summary of Findings

 **BorrowerRate:**
* Interest rates have a negative correlation with credit range. We see that the higher the CreditRange(Which means higher ProsperRating) the lower the interest rates on loans.
* We see the average and median interest rate on loans(BorrowerRate) Increasing with decreasing income range.
* Short term loans( a year or less) have lower interest rates on the average. long term(60month) loans have just very slightly higher interest rates on the average than medium term(36months). Medium term loans have more spread in interest rates recording highest and lowest interest rates.

**LoanStatus:**
 * Most of the Loans that are Current, Completed, Cancelled or are making final payments (FinalPaymentsInProgress) have on the average, lower Interest rates. Loans that are Past due, Defaulted or Charged off have on the average higher Interest rates. The average interest rates for LoanStatus that are past due are slightly higher with higher past due days. With Past Due(>120 days) having the highest mean Interest Rate.
* Loan Term plays a huge role with Loan Status. A great amount(89%) of the Short Term loan payments. have Completed Status. Compared to only 38% of Medium Term and only 9% of Long Term Loans. We see that the shorter the Term the more likely the loan is completed, Medium term loans are the most likely to be defaulted or Charged Off and Long Term loans are the most likely to have due payments followed by Medium Term Loans.
* The Loan Status is likely to be completed or Current when they are rated AA or A and we know that high CreditRange plays a role in being rated high(AA or A) in prosper ratings (alpha).

**OriginalLoanAmount:**
* the higher the original loan amount the less likely the payments are to be completed.
* Higher original loan amounts have slightly lower interest rates. and they are mostly associated with long term loans(60 months)

## Key Insights for Presentation

* We see that BorrowerRate seemed to correlate more strongly with some features like Loan Term, ProsperRating(Which showed a strong relationship with CreditScore) and weak with Debt-to-income-Ratio, income range and OriginalLoanAmount.
* We see that Original Loan amount seemed to have a negative and weak correlation with interest rates and are most associated with long term loans
* Overall the Outcome of a Loan(LoanStatus) seemed to have a high relationship with ProsperRating and hence CreditScoreRating. 
which means that People with less Debt-to-income-ratio, Higher Credit Rating and Lower interest rates complete their loans on time.
