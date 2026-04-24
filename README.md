
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
1. [Titanic Survival Prediction Using XGBoost](https://github.com/Thanuji-jpg/titanic)
2. [Project PrismCX: Customer Segmentation for IoT Smart Home Solutions](https://github.com/Thanuji-jpg/Smart-Entertainers/blob/main/Project%20PrismCX_ThanujaB.ipynb)
3. [Project PulseHR: Employee Trend Analysis Using Tableau](https://github.com/Thanuji-jpg/Employee-trends-)
4. [Project StreamIQ: Amazon Prime Content Analysis — Power BI Dashboard](https://github.com/Thanuji-jpg/business-intelligence-dashboard-suite)
5. [Instacart Market Basket Analysis & Reorder Prediction](https://github.com/Thanuji-jpg/InstaCart/blob/main/Predictions.ipynb)
6. [Project NeuroSeg: Brain Tumor Segmentation from MRI Using Deep Learning](https://github.com/Thanuji-jpg/Project-NeuroSeg-Brain-Tumor-Segmentation-from-MRI-Using-Deep-learning)   





[Titanic Survival Prediction Using XGBoost](https://github.com/Thanuji-jpg/titanic)

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


[Project PrismCX: Customer Segmentation for IoT Smart Home Solutions](https://github.com/Thanuji-jpg/Smart-Entertainers/blob/main/Project%20PrismCX_ThanujaB.ipynb)

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

Tableau Dashboard:

[Dashboard](https://github.com/Thanuji-jpg/Smart-Entertainers/blob/main/Customer_Segmentation.twbx): An interactive dashboard visualizes the full customer landscape with KPI tiles (total customers, average spend, churn rate, loyalty %), CORE segment distribution, RFM heatmap (recency vs. frequency), and churn risk overview. All components are interlinked and filterable by segment, region, age group, gender, and customer type.

Tools: Python (pandas), Tableau, GitHub

Recommendation
Smart home brands should tailor their engagement strategy to each CORE segment: deploy targeted onboarding campaigns for Convert customers, offer upsell and cross-sell promotions to Optimize customers, invest in loyalty programs for the Retain group, and trigger re-engagement sequences for Exit customers before they fully disengage. The Tableau dashboard enables marketing and sales teams to monitor these segments in real time and adjust campaigns dynamically — eliminating the guesswork from customer lifecycle management and maximizing retention ROI across the IoT product portfolio.


[Instacart Market Basket Analysis & Reorder Prediction](https://github.com/Thanuji-jpg/InstaCart/blob/main/Predictions.ipynb)

Business Problem
E-commerce grocery platforms like Instacart generate millions of transactions daily, creating a rich opportunity to understand and anticipate customer purchasing behavior. Predicting which products a customer is likely to reorder enables businesses to improve inventory planning, personalize product recommendations, and optimize marketing spend. This project analyzes Instacart's publicly available order dataset to uncover behavioral patterns and build machine learning models that accurately forecast product reorders.

Technical Details
[Dataset](: Instacart Market Basket Analysis from Kaggle — includes customer orders, products, departments, and aisle information across multiple order histories.
Phase 1 — Exploratory Data Analysis (Data Exploration.ipynb):
Examined dataset structure across orders, products, and user tables.
Handled missing values and identified data quality issues.
Analyzed purchasing patterns: order frequency, time-of-day trends, and reorder rates by department and aisle.
Visualized key distributions using histograms, bar plots, and heatmaps.
Phase 2 — Predictive Modeling (Predictions.ipynb):
Engineered features capturing user-product interactions, reorder ratios, days since prior order, and cart position behavior.
Trained and evaluated three classification models:
Logistic Regression — baseline model for interpretability.
Random Forest Classifier — captures non-linear feature interactions.
XGBoost Classifier — best-performing model based on AUC and F1 score.
Compared model performance using accuracy, F1 score, and AUC-ROC metrics.
Generated final reorder predictions on held-out test data.
Tools: Python (pandas, NumPy, scikit-learn, XGBoost, matplotlib, seaborn), Jupyter Notebook

Recommendation
Instacart and similar grocery platforms should leverage reorder prediction models to drive two core strategies: proactive replenishment — surfacing likely-to-reorder items at the top of a customer's next session — and targeted promotions for products with high reorder probability but recent drop-off in purchase frequency. XGBoost outperformed other models in this analysis, and further gains could be achieved by incorporating time-series features such as seasonality and rolling reorder windows. Integrating such a model into a real-time recommendation engine could meaningfully increase average order value and customer retention.

Project NeuroSeg: Brain Tumor Segmentation from MRI Using Deep Learning](https://github.com/Thanuji-jpg/Project-NeuroSeg-Brain-Tumor-Segmentation-from-MRI-Using-Deep-learning)

Business Problem
Accurate detection and segmentation of brain tumors from MRI scans is one of the most critical — and most challenging — tasks in medical imaging. Manual segmentation by radiologists is time-consuming, prone to inter-observer variability, and difficult to scale. This project applies deep learning to automate the segmentation of low-grade gliomas (LGG) from FLAIR MRI images, aiming to support clinicians with faster, more consistent tumor boundary detection and improve diagnostic outcomes.

Technical Details
Dataset: LGG MRI Segmentation dataset from Kaggle — FLAIR sequence brain MRI images with corresponding ground-truth tumor masks for low-grade glioma patients.
Task: Semantic image segmentation — predicting a pixel-wise binary mask identifying tumor regions within each MRI slice.
Deep Learning Architecture: U-Net — an encoder-decoder convolutional neural network designed specifically for biomedical image segmentation, preserving spatial detail through skip connections.
Key Steps:
Preprocessed FLAIR images: resizing, normalization, and augmentation to improve model generalization.
Split dataset into training, validation, and test sets.
Trained the segmentation model and evaluated using Dice coefficient and IoU (Intersection over Union) — standard metrics for medical segmentation tasks.
Visualized predicted masks against ground-truth annotations to assess qualitative performance.

Tools: Python, TensorFlow / Keras, NumPy, OpenCV, matplotlib

Recommendation

Deep learning-based segmentation models like U-Net demonstrate strong potential as a clinical decision-support tool — not to replace radiologists, but to accelerate their workflow and flag tumor boundaries as a second opinion. Hospitals and imaging centers handling high MRI volumes would benefit most from integrating such models into their diagnostic pipeline. Future improvements could include 3D volumetric segmentation across full MRI stacks rather than individual slices, and transfer learning from larger multi-institutional datasets to improve generalization across scanner types and patient demographics.

[Project PulseHR: Employee Trend Analysis Using Tableau](https://github.com/Thanuji-jpg/Employee-trends-)

*Business Problem*

Organizations with large workforces often struggle to identify early warning signs of attrition, disengagement, or imbalanced hiring — not because the data doesn't exist, but because it sits in spreadsheets without meaningful structure. This project analyzes 1,470 employee records to surface workforce trends across departments, education backgrounds, job satisfaction, demographics, and travel frequency. The goal is to give HR teams and business leaders a clear, visual picture of their people data so they can make proactive, evidence-based decisions around retention and hiring.

Technical Details
[Dataset](https://github.com/Thanuji-jpg/Employee-trends-/blob/main/Analyzing%20Employee%20Trends.csv) — 1,470 employee records with attributes including department, education field, gender, job satisfaction score, marital status, overtime, business travel frequency, and attrition status.
Key Findings from the Dashboard:
Department Distribution: R&D accounts for the largest share of employees, followed by Sales; HR has the smallest headcount — a potential resource gap worth monitoring.
Education & Job Satisfaction: Life Sciences employees report the highest average job satisfaction (~2.80), followed by Medical (~2.74), suggesting education field may influence workplace engagement.
Degree Type: The majority of employees hold Bachelor's or Master's degrees, with smaller representation from High School and Associate's-level qualifications.
Gender Distribution: Slightly more male employees (882) than female (588) — a gap that HR may want to address through targeted hiring initiatives.
Travel Frequency: Over 1,000 employees travel rarely, while a smaller subset travels frequently — frequent travel could be a contributing factor to attrition risk.
Notable Insight: Higher employee count does not consistently correlate with higher job satisfaction, suggesting headcount alone is not a reliable proxy for workforce health.

Tableau [Dashboard](https://github.com/Thanuji-jpg/Employee-trends-/blob/main/Tableau%20Dashboard.png): An interactive dashboard with filters for department, gender, marital status, and travel frequency — enabling HR teams to drill into specific workforce segments dynamically.

Tools: Tableau, CSV (cleaned in spreadsheet tools)

Recommendation
HR teams should prioritize two focus areas based on this analysis: first, investigate job satisfaction drivers in departments with high headcount but lower satisfaction scores — large teams with disengaged employees are a leading indicator of future attrition. Second, examine the gender distribution gap and travel frequency patterns as part of a broader diversity and retention review. Integrating attrition labels with satisfaction and travel data in a predictive model would be a strong next step, allowing the organization to shift from descriptive reporting to proactive workforce planning.
