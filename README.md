# Hospital Data Warehouse & Business Intelligence Analytics

A strategic hospital data warehouse and BI solution using DFM, star schema, OLAP, SQLite, SQL, Python and materialised views to analyse admissions, operation charges, length of stay and costs by Ward, Year and Quarter.


The project demonstrates how a hospital's operational healthcare data can be transformed into a dimensional data warehouse that supports efficient managerial analysis using Dimensional Fact Modelling (DFM), star schema design, OLAP analysis, SQL, SQLite, Python and materialised views.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Business Problem](#business-problem)
- [Business Questions](#business-questions)
- [Project Objectives](#project-objectives)
- [Project Workflow](#project-workflow)
- [Solution Overview](#solution-overview)

---

## Project Overview

This project develops a strategic hospital data warehouse designed to support business intelligence and managerial decision-making.

The solution focuses on hospital admissions and enables managers to analyse:

- charges per operation
- length of stay
- admission cost
- Secondary Diagnosis-related performance

across:

- Ward
- Year
- Quarter

The project applies data warehousing concepts including:

- Functional Dependency Analysis
- Attribute Tree construction
- Attribute Tree pruning and grafting
- Dimensional Fact Modelling (DFM)
- Star Schema design
- Fact and Dimension identification
- Measure identification
- OLAP analysis
- SQL aggregation
- Materialised views
- Query optimisation

The final warehouse was implemented using SQLite and validated using sample data and the two required managerial queries.

---

## Business Problem

Hospitals generate large volumes of operational data relating to patient admissions, treatment, diagnoses, wards, consultants, costs and time.

Although operational systems are suitable for recording individual transactions, managers require a different view of the data for strategic analysis.

The business intelligence challenge addressed in this project was therefore:

> How can hospital admission data be transformed into a structured analytical data warehouse that allows managers to efficiently analyse admission costs, operation charges and length of stay across wards and time?

The solution transforms the underlying operational data into a dimensional model optimised for analytical queries.

---

## Business Questions

The hospital management team identified two frequent queries.

### Q1 — Overall Admission Analysis

For each **Ward, Year and Quarter**, report:

- Charges per operation
- Length of stay
- Admission cost

### Q2 — Secondary Diagnosis Analysis

For each **Ward, Year and Quarter**, report:

- Charges per operation
- Length of stay
- Admission cost

for **Secondary Diagnosis**.

These two queries guided the dimensional modelling, measure selection and materialised-view design.

---

## Project Objectives

The main objectives were to:

1. Analyse the operational data and identify the main business fact.
2. Identify relevant entities and functional dependencies.
3. Construct an Attribute Tree.
4. Prune and graft the Attribute Tree according to the analytical requirements.
5. Build a Dimensional Fact Model from the resulting tree.
6. Identify dimensions, facts and measures.
7. Implement the DFM as a relational data warehouse.
8. Implement the warehouse using SQLite.
9. Insert representative sample data.
10. Design materialised-view support for the frequent managerial queries.
11. Execute and validate Q1 and Q2.
12. Demonstrate how dimensional modelling supports business intelligence analysis.

---

## Project Workflow

The complete project follows a structured data warehouse development process.

1. Business Requirements

Identify the managerial questions that the data warehouse must answer.

2. Business Fact Identification

Identify the main business event: ADMISSION

3. Functional Dependency Analysis

Analyse relationships between attributes and identify relevant determinants and dependencies.

4. Attribute Tree Construction

Transform the identified dependencies into an Attribute Tree.

5. Pruning and Grafting

Remove irrelevant branches and reorganise relevant attributes into meaningful analytical structures.

6. DFM Design

Identify:

- Fact
- Dimensions
- Measures
- Hierarchies

7. Star Schema Implementation

Translate the DFM into relational tables.

8. Sample Data

Insert representative data for validation.

9. OLAP Optimisation

Identify repeated analytical workloads and design a materialised view.

10. Query Validation

Execute Q1 and Q2 and verify that the warehouse produces the required results.

---

# Solution Overview

The project follows the following data warehousing workflow:

```text
Operational Healthcare Data
            │
            ▼
Functional Dependency Analysis
            │
            ▼
Attribute Tree
            │
            ▼
Pruning & Grafting
            │
            ▼
Dimensional Fact Model
            │
            ├── Dimensions
            ├── Fact
            └── Measures
            │
            ▼
Star Schema
            │
            ▼
SQLite Data Warehouse
            │
            ▼
Sample Data
            │
            ▼
Materialised View
            │
            ▼
OLAP Queries
            │
            ├── Q1
            └── Q2
