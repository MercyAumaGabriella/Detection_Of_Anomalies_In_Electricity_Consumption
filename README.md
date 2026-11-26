## Experimental Flow

The study implements an unsupervised machine learning pipeline for detecting anomalies in electricity purchasing and estimated consumption patterns among prepaid smart meter customers. The experimental workflow consists of eight stages:

| Stage | Description |
|---|---|
| **V1 – Data Auditing** | Inspect, clean and validate the original electricity transaction dataset. |
| **V2 – Feature Engineering** | Estimate electricity consumption and construct customer-week and customer-month behavioural features. |
| **V3 – Data Preprocessing** | Handle missing values, transform and scale features, and chronologically partition data into training, validation and testing sets. |
| **V4 – Feature Selection** | Apply Entropy-based Dependency Unsupervised Feature Selection (EDUFS) to rank behavioural features and evaluate feature subsets. |
| **V5 – Customer Clustering** | Apply K-Medoids clustering to identify customer behavioural groups and evaluate cluster quality and stability. |
| **V6 – Anomaly Detection** | Train Isolation Forest, Local Outlier Factor (LOF) and One-Class SVM using global and cluster-based approaches. |
| **V7 – Performance Evaluation** | Evaluate anomaly detection effectiveness using synthetic anomaly scenarios, precision, recall, F1-score, Average Precision and ROC-AUC. |
| **V8 – Robustness Evaluation** | Assess computational efficiency, memory utilization, scalability, threshold sensitivity, random-seed stability, consumption estimation sensitivity and model-level reproducibility. |

### Key Findings

Local Outlier Factor achieved the strongest overall detection performance on the weekly synthetic anomaly benchmark, with an Average Precision of **0.4042**, ROC-AUC of **0.8426**, and recall of **63.67%**.

The proposed pipeline supports anomaly screening in electricity purchasing and estimated consumption patterns. Validation against directly measured electricity consumption remains future work.
