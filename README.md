# Remediated Home Loan Approval Model

### Basic Information

* **Developer**: Nick Whims, `whimsnick@gmail.com`
* **Model date**: April, 2025
* **Model version**: 1.0
* **Model implementation code**: [DNSC_6330_loan_model.ipynb](https://github.com/nwhims/DNSC_6330/blob/main/DNSC_6330_loan_model.ipynb)

### Intended Use
* **Primary intended uses**: This model is a probability of default classifier, with an intended use case for determining eligibility for a hoem loan.
* **Primary intended users**: Home loan providers.
* **Out-of-scope use cases**: Any use beyond an educational example is out-of-scope.

### Training Data

* Data dictionary: 

| Name | Modeling Role | Measurement Level| Description|
| ---- | ------------- | ---------------- | ---------- |
|**term_360**| input | int | whether the mortgage is a standard 360 month mortgage (1) or a different type of mortgage (0) |
| **property_value_std** | input | float | value of the mortgaged property |
| **no_intro_rate_period_std** | input | int | whether (1) or not (0) a mortgage does not include an introductory rate period
| **loan_to_value_ratio_std** | input | float | atio of the mortgage size to the value of the property for mortgage applicants |
| **intro_rate_period_std** | input | float | standardized introductory rate period for mortgage applicants |
| **loan_amount_std** | input | float | standardized amount of the mortgage for applicants |
| **income_std** | input | float | standardized income for mortgage applicants. |
| **debt_to_income_ratio_missing** | input | int | missing marker (1) for debt_to_income_ratio_std |
| **debt_to_income_ratio_std** | input | float | standardized debt-to-income ratio for mortgage applicants |
| **conforming** | input | int | whether the mortgage conforms to normal standards (1), or whether the loan is different (0), e.g., jumbo, HELOC, reverse mortgage, etc. |
| **high_priced**| target | int | the annual percentage rate (APR) charged for a mortgage is 150 basis points (1.5%) or more above a survey-based estimate of similar mortgages; (1) = yes, (2) = no |

* **Source of training data**: Home Mortgage Disclosure Act (HMDA)
* **How training data was divided into training and validation data**: 62% training, 11% validation, 27% test
* **Number of rows in training and validation data**:
  * Training rows: 160,338
  * Validation rows: 19,831
