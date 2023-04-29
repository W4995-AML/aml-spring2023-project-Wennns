
# Applied Machine Learning Project Deliverable 3

## Bank Loan Modelling
AML Group 18 Section 2: Ji Qi(jq2365), Yizhi Liu(yl4993), Wen Song(ws2685)

### Data Sources
-   **Data Source Name**: Bank Loan Modelling
-   **Description**: 
	- ID: Customer ID
	- Age: Customer's age in completed years
	- Experience: the number of years of professional experience
	- Income: Annual income of the customer (USD 1000)
	- ZIPCode: Home Address ZIP code.
	- Family: Family size of the customer
	- CCAvg: Avg. spending on credit cards per month (USD 1000)
	- Education: Education Level. 1: Undergrad; 2: Graduate; 3: Advanced/Professional
	- Mortgage: Value of house mortgage if any. (USD 1000)
	- Personal Loan: Did this customer accept the personal loan offered in the last campaign? (1:Yes; 0:No)
	- Securities Account: Does the customer have a securities account with the bank?(1:Yes; 0:No)
	- CD Account: Does the customer have a certificate of deposit (CD) account with the bank? (1:Yes; 0:No)
	- Online: Does the customer use internet banking facilities? (1:Yes; 0:No)
	- CreditCard: Does the customer use a credit card issued by UniversalBank? (1:Yes; 0:No)
- **Data Summary**:
	- The dataset has data on  **5000**  customers.
	-   The dataset contains  **14 variables**  including  **13 independent variables**  and  **1 dependent variable**  which is  **Personal Loan**.
	-   There are **6 numeric variables**: ID , Age , Experience , Income , CC_Avg , Mortgage
	-   There are **3 categorical variables**: Family , Education , Zip_Code
	-   **5 Boolean variables** exist in the dataset: Personal_Loan , Securities Account , CD_Account , Online , Credit_Card
	-   There is no  **missing value**  in the dataset.
	-   There are no  **duplicates**  in the dataset.
	-   The dataset contains negative values for the  **Experience**, which need to be further processed.
- **Objective**:
The purpose of this project/dataset is to identify potential customers who have a higher probability of purchasing the loan.
-   **File Format**: Excel
-   **Data Collection Method**: The dataset is fetched from Kaggle. It is a dataset from a bank (Thera Bank) which has a growing customer base.
-   **Data Usage Restrictions**: This is no specific any restrictions or limitations on the usage of the data.
-   **Data Preprocessing**: 
	- Based on the Univariate Analysis, we need to drop all the noise records whose ‘Experience’ <0 or ‘ZIP Code’ < 5 digits.
	- Drop The variable ID, since it only acts as a customer identifier without adding any useful information to the dataset.
	- Drop ‘Age’ (strongly correlated with Experience.)
	- Log transformation will be applied to remove the right skewness in ‘Income’, ‘‘CCAvg’, and ‘Mortgage’(too many zeros and plus one before log transformation).
	- Convert ‘CCAvg’ average monthly credit card spending to annual spending by times 12 (Equal the unit in the Income)
	- Category Encoding will be selected to convert ‘Family’, ‘Education’ and ‘Zip Code’ into numerical values.
-   **Sample Data**: 
<img width="923" alt="Screenshot 2023-04-29 at 18 22 51" src="https://user-images.githubusercontent.com/42953950/235326677-2fc502a5-6844-4c44-9aa6-0aba02d5ab29.png">


