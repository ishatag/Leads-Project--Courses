**The AIM of the Courses Dataset:**
Analyze patterns in course enrollments and learner engagement, generate insights that help educators, platforms, and decision-makers improve course design, marketing strategies, and learner outcomes.
For example, a marketing team can understand which categories (e.g., Business, Tech) are bringing in the most students or revenue.

Stakeholders: 
1. Sales Team	: Focus efforts on Hot leads, save time by avoiding low-quality leads
2. Marketing Team	: Learn which campaigns and channels bring the best leads
3. Executives	: Get a clear overview of performance and lead quality via the Power BI dashboard
4. Data Analysts	: Use a structured, cleaned dataset and scoring logic for future improvement

**📁 Files Included in This Project**
data_analysis_leadscoring.py
Full Python code (Google Colab) for cleaning the data, analyzing trends, building ML models, and scoring leads.

lead_scoring_output_GoogleColab.csv
Final output file that includes lead score and category for each lead.

Leads Dashboard.pbix
Power BI dashboard showing lead behavior, source analysis, score categories, and performance summaries.

Leadscoring.csv & Lead Dictionary
A original version of the dataset.

**🛠️ Tools and Libraries Used**
Python: For data processing, visualization, and model building
Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn, xgboost

Google Colab: Python execution environment

Power BI: For stakeholder-facing visual dashboards

CSV files: For importing and exporting lead data

**🔍 Key Business Insights**
Lead source, time on website, and lead quality scores were major indicators of conversion.

ML models like Logistic Regression, Random Forest, and XGBoost were used and evaluated.

A Lead Score was created using model predictions and used to classify leads into:

a) Hot

b) Warm

c) Cold

Power BI was used to visualize the findings and allow business users to interact with the data easily.

**🧠 Python Script Breakdown: data_analysis_leadscoring.py**
This Python file includes a complete lead scoring pipeline:

 1. Data Preprocessing
Loaded and cleaned 9240 rows of raw lead data

Handled missing values, dropped irrelevant columns

Converted categorical variables using one-hot encoding

 2. Exploratory Data Analysis (EDA)
Analyzed key features: Lead Source, Country, Total Visits, Page Views

Plotted visualizations using matplotlib and seaborn

Identified features highly correlated with conversion

 3. Feature Engineering
Created new columns like:

lead_score (based on predicted probability)

lead_category: Hot (score > 0.7), Warm (0.4–0.7), Cold (< 0.4)

 4. Model Building & Evaluation
Applied and compared 4 models:

Logistic Regression

Decision Tree

Random Forest

XGBoost

Used train/test split (70/30) and metrics like:

Accuracy: Up to 85% with XGBoost

Precision/Recall/F1 scores to evaluate classification

Confusion matrix and ROC-AUC for deeper analysis

 5. Lead Scoring Output
Saved final leads with predicted scores and category to CSV

Ready to plug into CRM or dashboard tools

**📊 Power BI Dashboard Summary: Leads Dashboard.pbix**
The dashboard provides real-time insights for non-technical stakeholders:

🔹 Key Visuals:
Total Leads: 9,244

Conversion Rate: ~34.8%

Lead Categories:

Hot Leads: 2,180

Warm Leads: 3,094

Cold Leads: 3,970

🔹 Insights by Source:
Google and Direct traffic generated the highest number of Hot leads

Facebook had the lowest lead quality based on score

🔹 Conversion Funnel:
Shows drop-off from visitors → lead → qualified → converted

Helps identify weak points in the lead pipeline

🔹 Filters & Slicers:
Slice by Country, Lead Source, Category, and Time Period

**💼 Business Impact**
Sales teams can now prioritize better, focusing on leads that are more likely to convert.

Marketing teams can see which lead sources perform best and refine their campaigns.

Executives can track performance using a clean, visual dashboard that’s easy to use and understand.







