# Transaction-Based Customer Risk Assessment
# 1. Business Understanding

Financial institutions process a large volume of transactions every day, making it increasingly important to monitor customer activity and identify potentially unusual transaction patterns. Transactions that deviate from typical customer behavior may indicate potential financial risks, including suspicious activities or fraudulent transactions.

However, assessing transaction risk based on individual transactions can be challenging, particularly when customer activity varies in terms of transaction amounts, frequency, account balances, transaction channels, and other behavioral characteristics.

Without a structured risk assessment approach, financial institutions may struggle to distinguish between routine transaction behavior and activities that require additional attention. This can lead to inefficient monitoring processes and difficulties in prioritizing potentially risky transactions.

This project aims to develop a data-driven customer risk assessment approach by analyzing transaction patterns, segmenting customers into different risk categories, and building a classification model to automate risk categorization.

The analysis focuses on three key business questions:

- **How can customer transaction behavior be categorized?** Identify distinct transaction patterns based on financial activity, transaction frequency, account characteristics, and usage behavior.
- **Which transaction patterns require closer monitoring?** Distinguish between low, medium, and high-risk behavioral segments to help identify activities that may require further investigation.
- **How can risk assessment be made more efficient?** Develop an automated classification approach to categorize transaction activity and support more consistent risk monitoring.

# 2. Result Summary of the Project

The project analyzed approximately **2,537 raw transaction records**, covering transaction amounts, transaction types, account balances, transaction channels, customer demographics, and transaction timing.

After data preparation, 2,514 transaction records were retained for customer risk segmentation.

### Customer Risk Segmentation

Using transaction behavior analysis, the project identified three distinct risk segments:

| Risk Category | Transactions | Percentage |
|---|---:|---:|
| Low Risk | 860 | 34.2% |
| Medium Risk | 880 | 35.0% |
| High Risk | 774 | 30.8% |
| **Total** | **2,514** | **100%** |

The clustering analysis achieved a **Silhouette Score of 0.6007**, indicating a reasonably well-separated clustering structure.

### Key Segment Characteristics

- **Low Risk:** Characterized by relatively shorter transaction gaps and higher account balance categories, representing transaction behavior with comparatively lower risk indicators.
- **Medium Risk:** Shows longer transaction gaps compared to the low-risk segment, with relatively lower account balance characteristics, requiring additional monitoring.
- **High Risk:** Exhibits the longest average transaction gaps among the three segments, alongside relatively shorter transaction durations. These patterns are treated as potential risk indicators requiring further investigation.

### Classification Model Performance

Two classification algorithms were developed to automate the risk categorization process.

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| Decision Tree | 100% | 100% | 100% | 100% |
| Random Forest | 100% | 100% | 100% | 100% |

The Random Forest model was further optimized using GridSearchCV and achieved 100% testing accuracy.

These results demonstrate the model's ability to reproduce the clustering-based risk categories within the evaluated dataset. However, they should not be interpreted as 100% accuracy in detecting actual fraudulent transactions, since the target categories were generated through clustering rather than independently verified fraud labels.

# 3. Key Takeaways

- **Transaction behavior provides valuable risk indicators.** Transaction amounts, transaction frequency, account balances, and transaction durations can help identify differences in customer activity patterns.

- **Risk segmentation supports more targeted monitoring.** Dividing transaction activity into low, medium, and high-risk categories provides a structured approach to prioritizing monitoring efforts rather than treating every transaction equally.

- **High-risk segments require further investigation.** Transactions exhibiting unusual behavioral patterns can be flagged for additional review, allowing financial institutions to focus their attention on potentially suspicious activities.

- **Automated classification can improve operational efficiency.** Once behavioral risk categories have been established, classification models can help automate the categorization process and support more consistent risk assessments.

- **Risk indicators should not be treated as confirmed fraud.** Unusual transaction behavior does not necessarily indicate fraudulent activity. Additional verification and investigation are necessary before taking further action.

# 4. Process

- Importing the required Python libraries and loading transaction records containing financial activity, customer demographics, account information, and transaction behavior.
- Performing data understanding and exploratory analysis to examine transaction distributions, customer characteristics, financial activity, and potential anomalies.
- Conducting data preprocessing, including missing value handling, duplicate removal, outlier treatment, feature encoding, scaling, and transaction gap calculation to prepare the data for risk assessment.
- Performing customer risk segmentation using K-Means clustering to identify distinct transaction behavior patterns and categorize them into low, medium, and high-risk groups.
- Analyzing cluster characteristics to understand differences in transaction amounts, account balances, transaction frequency, and other behavioral indicators.
- Developing and comparing Decision Tree and Random Forest classification models to automate risk categorization, followed by hyperparameter tuning and model evaluation.

# 5. Solution Statement

This project proposes a transaction-based risk assessment approach that combines behavioral segmentation and automated classification to support financial risk monitoring.

By identifying distinct transaction behavior patterns and categorizing them into different risk levels, the proposed approach provides a structured way to recognize potentially unusual activities and prioritize transactions for further review.

The solution can serve as a foundation for a risk monitoring framework that enables financial institutions to:

- Segment transaction activity based on behavioral risk indicators.
- Identify potentially unusual transaction patterns that require additional investigation.
- Prioritize monitoring efforts based on assigned risk categories.
- Automate the initial risk categorization process to improve operational efficiency.
- Support data-driven decisions in financial risk management and fraud prevention.

Ultimately, the objective is to move from reactive transaction monitoring toward a more structured, data-driven risk assessment process that helps financial institutions identify potential threats and allocate monitoring resources more effectively.
