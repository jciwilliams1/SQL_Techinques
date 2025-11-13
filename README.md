# SQL Fundamentals for Data Analysis
<img width="324" height="324" alt="Image" src="https://github.com/user-attachments/assets/ee991e7f-a5de-4adf-a728-b211d91bfe85"/>

### Purpose of the Project

This project provides a structured collection of SQL scenarios that progress from foundational querying techniques to intermediate analytical skills. The scenarios simulate real business questions and focus on selecting data, applying conditional logic, organizing results with ORDER BY, creating calculated fields and aggregate values, and summarizing data using GROUP BY and HAVING.

The goal is to demonstrate the ability to apply SQL to practical data problems while showcasing clear reasoning, accurate analytical logic, and well-organized query structure.

### Skills Demonstrated
This project highlights the ability to:
- <b>Retrieve and explore data using SELECT statements</b>
- <b>Work within relational database structures using databases, schemas, and tables</b>
- <b>Apply filtering logic using comparison, range, and set-based operators in WHERE and HAVING</b>
- <b>Sort and organize results using ORDER BY and apply limits when appropriate</b>
- <b>Create calculated and derived fields using numeric, text, and date operations</b>
- <b>Use aggregate functions to summarize data</b>
- <b>Categorize and summarize results using GROUP BY</b>
- <b>Interpret business questions and translate them into SQL solutions</b>


## SQL Project 1 – Older clients in warm-weather states

**Scenario:**  
A retirement-planning specialist wants a focused list of older clients who could be invited to in-person events in warmer regions. She asks you to pull each person’s internal customer number, first and last name, current age, home city, state, phone contact, and email address for individuals who are between 60 and 75 years old, live in Texas, Florida, or Arizona, are recorded as either Female or Other, are not based in Boston or Chicago, and whose internal customer number falls between 5 and 20.

**Focus:** Filtering on multiple demographic conditions and sorting results (`SELECT`, `WHERE`, `BETWEEN`, `IN`, `NOT IN`, `ORDER BY`)

<img width="420" height="384" alt="Image" src="https://github.com/user-attachments/assets/51a04140-3b77-4cbc-a5bc-fa35c093acb2" />


## SQL Project 2 – Younger urban clients for mobile banking 

**Scenario:**  
The digital banking team is designing offerings for younger, city-based clients who are likely to favor mobile channels. They want the internal customer number, first and last name, age, city, state, phone contact, and email address for people between 25 and 40 years old who live in a large city such as New York, Los Angeles, Chicago, San Diego, or Dallas, are recorded as Male, are located in states like California, Texas, or Pennsylvania, and whose customer number is between 1 and 20.

**Focus:** Applying multi-criteria filters with ranges and city lists, then ordering results (`SELECT`, `WHERE`, `BETWEEN`, `IN`, `ORDER BY`)

<img width="704" height="348" alt="Image" src="https://github.com/user-attachments/assets/17e1bb8e-dfe9-4e6f-835b-57f3c2e12a24" />


## SQL Project 3 – Estimating simple monthly payments for consumer loans

**Scenario:**  
A lending analyst is reviewing approved unsecured consumer borrowing and wants to understand the approximate monthly obligation associated with each record. She needs a table showing each internal loan reference, the product category, total principal, term length, and annual rate, along with a field that reflects the estimated monthly obligation used for early-stage affordability reviews. She plans to look at the loans with the highest monthly expectations first.

**Focus:** Filtering approved loans and creating a simple calculated payment field, ordered by the calculated value (`SELECT`, `WHERE`, calculated fields, `ORDER BY`)

<img width="558" height="245" alt="Image" src="https://github.com/user-attachments/assets/af337ff8-b060-498a-bc09-40218ed0909c" />


## SQL Project 4 – Mid-sized unsecured loans

**Scenario:**  
Another analyst is preparing material for a discussion about smaller unsecured borrowing. She needs branch identifier, loan reference number, amount, yearly rate, term in months, key decision date, and current status for records that represent the personal-borrowing type, have amounts between 5,000 and 25,000, terms between 12 and 48 months, yearly rates greater than 0.04, decision dates between '2021-01-01' and '2023-12-31', and statuses of either Approved or Closed.

**Focus:** Using range filters on amounts, terms, rates, and dates, plus status filters, then sorting by rate and amount (`SELECT`, `WHERE`, `BETWEEN`, comparison operators, `IN`, `ORDER BY`)

<img width="639" height="366" alt="Image" src="https://github.com/user-attachments/assets/88ef2d74-81b4-4769-b9c8-f868a54be901" />


## SQL Project 5 – Branches handling larger deals on average

**Scenario:**  
Regional leadership wants to understand which locations tend to handle larger lending deals on average. They ask for a summary that shows one row per branch with the typical principal size and the total number of records for that location. Only branches whose typical principal exceeds 30,000 should remain in the final results, and leadership wants to quickly see which locations are working with the biggest typical amounts near the top of the report.

**Focus:** Aggregating loan amounts by branch and filtering with `HAVING` to keep only higher-average locations (`SELECT`, aggregate functions, `GROUP BY`, `HAVING`, `ORDER BY`)

<img width="436" height="206" alt="Image" src="https://github.com/user-attachments/assets/50922121-1216-46fa-b534-30754e441170" />


## SQL Project 6 – Product types with unusually low typical balances

**Scenario:**  
Risk management suspects that some product categories may be more prone to very low balances, which can indicate financial stress or disengagement. They want a summary that shows each product category and its typical balance level, but they only want to see categories where that typical balance falls below 3,000. The output should make it easy to see which categories have the lowest typical balances.

**Focus:** Summarizing account balances by product type and isolating low-typical-balance categories (`SELECT`, aggregate functions, `GROUP BY`, `HAVING`, `ORDER BY`)

<img width="435" height="194" alt="Image" src="https://github.com/user-attachments/assets/5b2b4058-c8a0-4919-94ed-2012e5bef099" />


## SQL Project 7 – Medium-balance activities with risk buffers 

**Scenario:**  
A treasury analyst is reviewing how certain account activities impact customers with medium-sized balances. She needs a list of movements containing the internal transaction reference, the activity date, the category of movement, the amount involved, and the balance recorded afterward. She also wants a field showing a projected 5% buffer amount based on the value of each movement to support a risk-adjustment review. Only activities that involve deposits or withdrawals, took place during 2023, involve amounts of at least 700, and lead to balances above 2,000 should appear. She plans to begin her analysis with entries that carry the largest projected buffer amounts.

**Focus:** Filtering transactions by type, date, amount, and resulting balance while computing a risk buffer metric (`SELECT`, `WHERE`, `IN`, date range filtering, calculated fields, `ORDER BY`)

<img width="590" height="279" alt="Image" src="https://github.com/user-attachments/assets/3fdfa3ee-48b8-46ca-9c90-dff456fe15c0" />


## SQL Project 8 – Revolving credit utilization review  

**Scenario:**  
The card portfolio team is studying how customers are using revolving credit. They want a report showing the internal card identifier, the branded product type, total line amount, outstanding balance, required minimum payment, next scheduled due date, and most recent recorded payment activity. They also want a field that represents the portion of the total line currently being used, allowing them to estimate relative utilization. Only cards with total lines of at least 5,000, balances over 1,500, minimum payments above 50, and next due dates within 2023 should appear. Review will begin with those showing the highest utilization portion.

**Focus:** Filtering card records on line, balance, payment, and due date while calculating and ranking utilization (`SELECT`, `WHERE`, date range filtering, calculated fields, `ORDER BY`)

<img width="598" height="316" alt="Image" src="https://github.com/user-attachments/assets/2aa5bffc-5f7f-4e96-9c35-2fa9e4aa48db" />


## SQL Project 9 – Low utilization but high limits

**Scenario:**  
A marketing analyst wants to identify cardholders who have sizeable credit lines available but relatively small outstanding balances for cross-sell opportunities. The analyst requests card identifier, product brand, total line amount, outstanding balance, required minimum payment, next due date, most recent payment date, and reward balance for entries where the total line is at least 7,000, the balance is less than 2,000, the required minimum payment is under 100, the next due date falls within 2023, the brand is either MasterCard or AMEX, and the reward balance is under 5,000.

**Focus:** Identifying cross-sell candidates with high limits and low balances using multi-criteria filters on amounts, dates, brands, and rewards (`SELECT`, `WHERE`, date range filtering, `IN`, comparison operators, `ORDER BY`)

<img width="592" height="345" alt="Image" src="https://github.com/user-attachments/assets/4f06e5d7-699b-458d-8839-6b06892a80ab" />


## SQL Project 10 – Non-married clients in specific occupations

**Scenario:**  
Another campaign focuses on non-married or separated household situations. The analyst wants row identifier, occupation category, marital description, and education level for records in which the marital description is single or divorced, the occupation category is one of services, blue-collar, or entrepreneur, the education level is one of basic.4y, basic.6y, or basic.9y, the marital description is not married, and the occupation is not recorded as unknown.

**Focus:** Applying categorical filters with inclusion and exclusion logic, then sorting by marital status and occupation (`SELECT`, `WHERE`, `IN`, `!=`, `ORDER BY`)

<img width="558" height="274" alt="Image" src="https://github.com/user-attachments/assets/e9df47d7-b697-454f-b776-9610b71f4c82" />





