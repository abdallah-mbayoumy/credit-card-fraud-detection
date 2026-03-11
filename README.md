# Credit Card Fraud Detection - Data Governance Project

This project focuses on applying data governance principles to a credit card fraud detection dataset. The work includes data profiling, data quality assessment, privacy protection techniques, anonymization, and governance controls.

## Dataset Description

The dataset contains anonymized credit card transaction data. Most features (V1–V28) are results of PCA transformation for privacy protection.

Columns include:

- Time: Time elapsed between transactions
- V1 – V28: PCA transformed features
- Amount: Transaction amount
- Class: Target variable (0 = Normal transaction, 1 = Fraud)

## Project Components

The project is divided into several data governance modules.

### 1. Data Profiling

Data profiling was performed using:

- Sweetviz
- YData Profiling
- DataProfiler

These tools provide insights into:

- Data distribution
- Missing values
- Data types
- Feature statistics
- Data quality overview

### 2. Data Quality Validation

Data quality checks include:

- Duplicate detection
- Missing value analysis
- Outlier detection using IQR
- Schema validation using Pandera
- Rule-based validation using Cerberus

Example checks:

- Time must be ≥ 0
- Amount must be ≥ 0
- Class must be either 0 or 1

### 3. Data Privacy and Security

Multiple privacy-preserving techniques were implemented:

Encryption
- Fernet symmetric encryption

Hashing
- SHA256 hashing for anonymization

Pseudonymization
- Masking sensitive attributes

Generalization
- Converting Time and Amount into ranges

Randomization
- Adding noise to numerical data

Data masking
- Generating synthetic values using Faker

### 4. Access Control (RBAC)

A Role-Based Access Control system was implemented to manage user permissions.

Roles included:

- jr_editor
- editor
- it

Permissions included:

- read
- create
- update
- delete

### 5. GDPR Compliance

Basic GDPR compliance simulation includes:

- Anonymization of sensitive data
- Consent tracking
- Data deletion verification
- Compliance checking functions

## Technologies Used

Python

Libraries:
- pandas
- numpy
- sweetviz
- ydata-profiling
- dataprofiler
- pandera
- cerberus
- cryptography
- faker
- matplotlib
- seaborn

## Project Structure

