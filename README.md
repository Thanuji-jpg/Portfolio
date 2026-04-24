
# Thanuja Babu - Data & ML Portfolio

Hi! I am Thanuja, a Data & ML Engineer with 2+ years of experience 
across customer insights, predictive analytics, and data engineering. 
I have worked as a Data Engineer, AI & Data Science Intern, and 
Customer Insights Analyst, giving me a well-rounded view of the 
full data lifecycle — from pipelines to business decisions.

One of my key areas of experience is edtech, where I worked on 
website optimization to improve user engagement and course 
performance using data-driven strategies. I am also passionate 
about healthcare analytics and customer insights — domains where 
data can create real, meaningful impact.

I work with Python, SQL, Tableau, and Power BI to build predictive 
models, data pipelines, and interactive dashboards that turn messy 
data into clear stories.

I am currently open to roles in Data Analytics, Data Science, 
Analytics Engineering, and Business Intelligence.

#CONTENTS:
1. [Titanic Survival Prediction Using XGBoost](titanic-notebook.ipynb)
2. [Smart-Entertainers](Project PrismCX_ThanujaB.ipynb)


[Titanic Survival Prediction Using XGBoost](titanic-notebook.ipynb)

Business Problem
The sinking of the Titanic is one of the most infamous maritime disasters in history, resulting in the deaths of over 1,500 passengers and crew. Understanding which factors contributed to survival — such as passenger class, age, gender, and fare — can offer insights into human decision-making, social inequalities, and emergency response effectiveness. This project builds a machine learning model to predict passenger survival based on available demographic and ticket information.

Technical Details
[Dataset](test.csv)
[Dataset](train.csv) : Titanic dataset from Kaggle — 891 training records with features including passenger class, sex, age, fare, embarkation port, and cabin information.
Data Preprocessing:
Handled missing values: median imputation for Age, mode imputation for Embarked, dropped Cabin due to high missingness.
Encoded categorical features: Sex and Embarked converted using label encoding.
Dropped non-predictive columns: Name, Ticket, PassengerId.
Model Used: XGBoost Regressor — trained on an 80/20 train-test split with predictions thresholded at 0.5 for binary classification.

Evaluation Metrics:
Accuracy score and confusion matrix to assess classification performance.
Feature importance chart to identify the strongest predictors of survival.

Key Findings:
Sex was the most influential feature — female passengers had significantly higher survival rates.
Passenger class (Pclass) and Fare were strong secondary predictors, reflecting socioeconomic disparities in evacuation access.
Age showed moderate importance, with children having a higher likelihood of survival.
Tools: Python (pandas, NumPy, XGBoost, scikit-learn, seaborn, matplotlib)

Recommendation
The model demonstrates that survival on the Titanic was heavily influenced by gender and socioeconomic status, with first-class female passengers having the highest survival probability. For emergency preparedness practitioners, this analysis underscores the importance of equitable evacuation protocols that do not inadvertently disadvantage passengers based on class or location on the vessel. Future work could incorporate XGBoost Classifier (instead of Regressor) for more appropriate binary output, and hyperparameter tuning via grid search to further improve accuracy.

[Project PrismCX: Customer Segmentation for IoT Smart Home Solutions](Project PrismCX_ThanujaB.ipynb)

Business Problem
Smart home automation brands operate in a highly competitive IoT market where understanding customer behavior is critical to sustainable growth. Without a structured segmentation model, businesses risk applying generic marketing strategies that fail to address the distinct needs of new, loyal, at-risk, and disengaged customers. Project PrismCX addresses this gap by combining RFM analysis (Recency, Frequency, Monetary) with the CORE framework — Convert, Optimize, Retain, Exit — to deliver a precise, actionable classification of the customer base and surface it through an interactive Tableau dashboard.

Technical Details
Dataset: [Dataset](Original_Dataset(Smart Entertainer for customers).csv)— 2,200+ transaction records covering customer demographics (age group, gender, region), IoT device purchase history, and derived RFM metrics.
Data Preparation:
Cleaned and normalized smart device transaction data using Python (pandas).
Derived Recency, Frequency, and Monetary values per customer from raw transaction records.
Scoring & Tagging:
Assigned R, F, and M scores on a 1–4 scale using quantile binning.
Created behavioral tags: First-time vs. returning customer, top spender (top quartile), loyalty identifier (based on frequency + recency), and churn risk flag (inactivity-based).
CORE Segmentation: Each customer was classified into one of four strategic segments:
Convert — New or low-engagement customers requiring activation.
Optimize — Moderate spenders with untapped growth potential.
Retain — High-value, frequent buyers who drive core revenue.
Exit — At-risk customers showing signs of disengagement.
Tableau Dashboard [Dashboard](Customer_Segmentation.twbx): An interactive dashboard visualizes the full customer landscape with KPI tiles (total customers, average spend, churn rate, loyalty %), CORE segment distribution, RFM heatmap (recency vs. frequency), and churn risk overview. All components are interlinked and filterable by segment, region, age group, gender, and customer type.
Tools: Python (pandas), Tableau, GitHub

Recommendation
Smart home brands should tailor their engagement strategy to each CORE segment: deploy targeted onboarding campaigns for Convert customers, offer upsell and cross-sell promotions to Optimize customers, invest in loyalty programs for the Retain group, and trigger re-engagement sequences for Exit customers before they fully disengage. The Tableau dashboard enables marketing and sales teams to monitor these segments in real time and adjust campaigns dynamically — eliminating the guesswork from customer lifecycle management and maximizing retention ROI across the IoT product portfolio.
