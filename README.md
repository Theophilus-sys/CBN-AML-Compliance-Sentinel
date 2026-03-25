# CBN Sentinel: An AI powered AML Compliance Engine
**Automated Anti-Money Laundering (AML) & Suspicious Activity Reporting (SAR)**

## The Context
In 2024, the Central Bank of Nigeria mandated that all financial institutions that is banks, Fintechs e.t.c deployed real-time AML systems. With an 18-24 month compliance window, the industry is shifting from manual oversight to an AI-driven deterrence.

## "The Sentinel" 
This project is an end-to-end prototype of a modern compliance engine. It solves two critical problems:
* 1. **Detection:** The usage of Machine learning to identify suspicious transactions that human eyes could miss.
  2. **Reporting:** Using Generative AI to instantly draft a formal **Suspicious Activity Reports (SAR)** suitable for CBN submission.

## Tech Stack
* 1. Python & Scikit-Learn: For the implementation of **Isolation Forest** model for unsupervised anomaly detection.
  2. Large Language Models (LLMs): For the automation of the legal narrative for flagging transactions.
  3. Pandas: For the processing of high-volumne synthetic Nigerian fintech transactions.
  4. Streamlit: For the deployment of real-time monitoring dashboard for Compliance officers.

## Core Features
* 1. Anomaly Scoring: The end-product of this project can be able to detect round numbers traps, location spoofing, and sudden velocity spikes in funds transfer.
  2. One-Click SAR: The end product of this project can convert raw transaction metadata into a professional, legally-structured report.
  3. Compliance Heatmap: The end-product of this project can visualize high-risk zones for money laundering in real-time.

## Project's Impact
Through the automation of the detection-to-report pipeline, "The Sentinel" aims at reducing the time spent on the filing of a single suspicious case from **30 minutes to 5 minutes** and also ensuring that 100% compliance can be attained with zero human fatigue.
### Task Two: Data Importation, Feature Enginnering, Data Splitting
For the identification of velocity spikes, scaling round numbers, preprocessing categorical data
- The Amount column is enginnered for the flagging of Round number amount, flagging of ammounts above CBN's Five Million Threshold for Individuals and Ten Million Threshold for Corporations.
- Timestamp for the counting of transactions from a particular user in an hour
- Transaction Type for the understanding of different transactions and assigning of high risk scores to specfic locations

- ### Model Selection and Training
For this project the best to use is the "Champion Challenger". Random Forest is selected as the baseline model for measuring the performance of even complex models. debugging features, checking model overkill not requiring heavier ml models, quantifyingg improvements
- Xgboost is the industry standard for stuctured tabular data. it builds trees squentially with each tree correcting the errors of the previous ones. this makes it good fore catching subtle fraud cases that basic models miss. it also handles imbalances in a dataset.
- Logistic Regression is for explanability. as it provides clear coefficients that is weights for every feature. it is also mathematically simple
- Isolation forest is for the unknown detection. it doesn't look at labelled columns to carry out any operation as it looks at data points that are different from everything else.

- Task Three: AI Model Integration
In line with CBN's Baseline Standards for Automated AML Solutions which specifically mandates that financial institutions automate reporting to the Nigerian Financial Intelligence Unit (NFIU) within strict timelines. Writing a Supicious Activity Report using Groq LLM takes a compliance officer up to 45 minutes, this can be reeduced to five minutes
