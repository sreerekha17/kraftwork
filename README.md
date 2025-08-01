# Exploratory Data Analysis Using Concepts of Machine Learning: Will the customer Accept the coupon ?

**Link to Assignment Notebook** - https://github.com/sreerekha17/kraftwork/blob/main/prompt.ipynb

##  Project Overview  
This project explores **drivers’ behavior towards coupon acceptance** based on user, contextual, and coupon attributes.  

The dataset contains information such as:  
- **User attributes** → age, gender, income, marital status, bar/restaurant visits  
- **Contextual attributes** → weather, time of day, passengers, Driving destination  
- **Coupon attributes** → coupon type, time before expiration  

The goal is to:  
1. Understand which factors influence **coupon acceptance**  
2. Compare acceptance rates across **different user segments**  
3. Visualize key behavioral patterns  

## Files  

- `data/coupons.csv` → Original dataset  
- `prompt.ipynb` → Notebook with full analysis  
- `images/*` → Generated visualizations  


## Tools & Libraries  

This analysis was performed using **Python** with the following libraries:  

- [pandas](https://pandas.pydata.org/) → data cleaning, preprocessing, grouping  
- [numpy](https://numpy.org/) → numerical operations  
- [matplotlib](https://matplotlib.org/) & [seaborn](https://seaborn.pydata.org/) → visualizations  
- [jupyter notebook](https://jupyter.org/) → interactive exploration  


## Techniques & Concepts Applied

### 1. Data Cleaning & Preprocessing  
- Handling **missing values** (drop/impute)  
- Creating **derived features* (used appropriate methods like mean)
- Converting **categorical values** into standardized groups  (eg 1~3 -> (1 + 3)/2)

### 2. Descriptive Statistics  
- `groupby` aggregations to calculate **acceptance rates**  
- Comparing groups such as:  
  - **Below vs above income**  
  - **Age < 30 vs older drivers**  

### 3. Conditional Segmentation  
- Filtering with **multiple conditions**:  
  - Goes to bars more than once a month & not widowed & no kids  
  - Goes to bars more than once a month & under age 30  
  - Goes to cheap restaurants more than 4 times a month & income below 50k

### 4. Visualization  
- **Bar plots** → acceptance rates per segment
- **Pie Charts** → acceptance rates per segment  
- **Stacked bars** → accepted vs rejected counts  
- **Histograms** → feature distributions  
- **Heatmaps** → multi-dimensional acceptance patterns  


##  Insights  
- Compares the likelyhood of accepting bar coupon when travelling with no kids, who are a frequent bar visitor and relatively younger 
- Also compares the impact of <ins>weather</ins>, <ins>income</ins>, <ins>marital status<ins>, <ins>travelling destination and urgency</ins>, traveling with friends/alone on coupon acceptance

- Bar Coupon Acceptance 

<img width="600" height="600" alt="bar-coupons-acceptance" src="https://github.com/user-attachments/assets/f6757483-199d-4aa7-bdf0-a7e9e35adac6" />

 -  Various coupons 

<img width="800" height="600" alt="coupons_data_as_pie" src="https://github.com/user-attachments/assets/f0e85d9e-0acd-4ebc-a01b-a7c45df2a19f" />

- Destination Impact 
<img width="640" height="480" alt="destination-urgency-impact" src="https://github.com/user-attachments/assets/f021a7b5-6799-4bc0-941f-dba84e995810" />


- Passenger Impact 
<img width="640" height="480" alt="passanger-impact_point-plot" src="https://github.com/user-attachments/assets/8dca0328-c58a-467e-90f1-10386c238f85" />

## Summary of Findings
- Observed that sunny weather, non urgent travels, traveling with friends and partners, coupons to carry outs and restaurants with less than $20 has \n stronger influence on accepting coupons

## Next Steps
- Collect more similar data and perform detailed analysis
- Integrate with an app that sends targeted personaized coupons based on predicted acceptance probability such as weather, time of the day, travel destination and so on.



