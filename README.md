# Ecommerce_MarketMixModel_Eleckart_Linear_Regression
 As a data scientist or an analyst working for ElecKart, we need to develop a market mix model based on the given information and the data sets related to consumer purchases, monthly spends on advertising channels, climatic information and the NPS/stock index.
 
## Table of Contents
  * [What: Project Overview](#what-project-overview)
  * [Why: Motivation](#why-motivation)
  * [How: Process Involved](#how-process-involved)
  * [Project Problem Statement Description](#project-problem-statement)
  * [Project Installation_Steps](#project-installation-steps)
  * [Directory Tree](#directory-tree)
  

## WHAT: Project Overview 
As a data scientist or an analyst working for ElecKart, we need to develop a **Market Mix Model based** on the given information and the data sets related to consumer purchases, monthly spends on advertising channels, climatic information and the NPS/stock index. We will be using Python as the programming language.

## WHY: Motivation
This project is the **FINAL CAPSTONE PROJECT**, part of Upgrads PGDDS(Post Graduate Program in Data Science) with IIITB University Bangalore

## HOW: Process Involved
- This section mentions EDA Process, ML algorithms, Libraries, stragtegy used if any etc
- I have made a **PPT PRESENTATION** of this project, can be viewed on **slide share** here:** Also under `/presentations` directory (See directory structure below)
- I also have a **VIDEO EXPLANATION** which explains the process EDA, Feature Engineering, Linear Regression Models built, Model Selection and Evaluation, can be viewed here: also under `/presentations` directory(See directory structure below)
- I have built additive and multiplicative Linear Regression Models for this market mix modelling.
- Koyck and Distributed lag models could be built and have parked them for future if time permits.

## Project Problem Statement

### Problem Statement

As a data scientist or an analyst working for ElecKart, you need to develop a market mix model based on the given information and the data sets related to consumer purchases, monthly spends on advertising channels, climatic information and the NPS/stock index.

<!--![lead_funnel_image](./presentations/images/lead_funnel_image.jpg?raw=true "Leads Funnel") -->
<!-- ![lead_funnel_image](https://user-images.githubusercontent.com/14209223/149206507-62bf586c-e02b-41fc-9674-44aa3bb8931c.jpg) <!-- I simply dragged and dropped the image-->

### Data Understanding
You have to use the data from July 2015 to June 2016. The data consists of the following types of information:

**Order level data**

- FSN ID: The unique identification of each SKU
- Order Date: Date on which the order was placed
- Year/Month: Year and month when the order was placed
- Order ID: The unique identification number of each order
- Order Item ID: When the customer orders two different products at the same time, the system generates two different order Item IDs under the same order ID. Note that orders are tracked using Order Item IDs.
- GMV: Gross merchandise value or revenue
- Units: Number of units of the specific product sold
- deliverybdays: Number of business days between the placement of the order and the final delivery day
- deliverycdays: Number of calendar days between the placement of the order and the final delivery day
- Order Payment Type: How the payment was made, whether prepaid or cash on delivery
- SLA: Number of days it typically takes to deliver the product
- Cust id: Unique identification of a customer
- pincode: Pin location from where the order was placed
- product_analytic_super_category: Super category to which the product belongs
- product_analytic_category: Category to which the product belongs
- product_analytic_sub_category: Sub-category to which the product belongs
- product_analytic_vertical: Assortment vertical to which the product belongs
- Product MRP: Maximum retail price of the product
- Product procurement SLA: Time typically taken to procure the product

**Apart from this, the following information is also available:**

- Monthly spend on various advertising channels
- Days when there was any special sale on products
- Monthly NPS score (this may work as a proxy to the ‘voice of the customer’)
- Stock index of the company on a monthly basis 
- Climatic information of Ontario during 2015 and 2016

### Project Pipeline
The project pipeline can be briefly summarised in the following steps:

### Data Preparation
You have to create market mix models for three product subcategories: Camera Accessory, Home Audio, and Gaming Accessory. Also, the models must be built at a weekly level for each of the subcategories.

### Feature Engineering
As the e-commerce company is based in the Ontario region, we will need to include its climate data to analyse whether it has any effect on the company’s revenue. Create as many features as possible with the available data.

Note: Create separate columns for Pay Date (if the first or fifteenth of the month) and holidays by creating a flag as a 0 or 1. For example, if it’s a holiday, the value will be 1.

### Exploratory Data Analysis
Perform univariate analysis, bivariate analysis, correlations, cross-tabs, and create visualisations on the pre-analytical data set. Obtain insights and shortlist variables for modelling. Create the KPIs according to the requirement of the model and write appropriate comments for choosing those KPIs.

### Model Building and Evaluation
Build basic, logarithmic, and multiplicative models or any other possible model with the available data set and fine-tune their hyperparameters until you get the desired level of performance. Analyse the impact of various attributes on the target variable using appropriate metrics. 

### Presentation of Results
Choose the best results of the market mix model for each of the three product subcategories and create a PowerPoint presentation along with a video explaining the analysis and results to the relevant business stakeholders such as CMO/CFO.

The audience should be able to intuitively understand the model/analysis that you have built/performed and its financial impact on the business. Point out any surprising or unexpected trends that you notice.

## Project Installation Steps
- The input data is large and greater than 100mb which cannot be uploaded/commited by using normal GIT. Have to use GIT LFS. 
- Instead of using GIT LFS I have just compressed the data files and placed in under `/data/raw`. You need to unzip it and placed all files under the same path of `/data/raw` for the project to be tidy and work.

<!--## Directory Tree 
```
├── app 
│   ├── __init__.py
│   ├── main.py
│   ├── model
│   ├── static
│   └── templates
├── config
│   ├── __init__.py
├── processing
│   ├── __init__.py
├── requirements.txt
├── runtime.txt
├── LICENSE
├── Procfile
├── README.md
└── wsgi.py
```
-->

## Directory Tree
```
|--   app
|     |-- Readme.md 
|     |-- notebooks -- main.py <-This is the main python jupyter notebook where execution of project starts
|     |-- data <-- If this folder is absent,data is larger than 100mb, thus have to use GIT LFS
|          |-- raw --  <- This has input data for the project
|     |-- references <- This has Data dictionaries, manuals, and all other explanatory materials.
|     |-- reports <- Generated analysis as HTML, PDF, LaTeX, etc.
|           |-- figures <- Generated graphics and figures to be used in reporting
|     |-- presentations <-Manually created presentations for business users,stake holders in pptx,pdf etc
|           |-- images <- Manual images obtained from various sources for presentation & other checkpoints
```
