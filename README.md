# Correlation-Analysis-of-Website-Features
This project builds a machine learning model to detect phishing websites using features like URL structure, domain details, and website behavior. With over 11,000 samples, it uses data analysis and classification techniques to achieve high accuracy, helping improve cybersecurity by identifying malicious websites.


# Phishing Website Detector

## Abstract
Phishing websites pose a significant threat to internet users by imitating legitimate websites to steal sensitive information. This project aims to develop a machine learning model that can accurately detect phishing websites using a dataset containing various website features. By applying data analysis and classification techniques, the model helps in identifying whether a given website is legitimate or malicious.

## Introduction
Cybersecurity threats like phishing continue to rise, targeting users through deceptive websites that appear genuine. Automated detection systems can greatly aid in reducing human error and increasing web safety. In this project, we explore how machine learning can classify websites based on their characteristics and flag them as phishing or legitimate.

## About the Dataset
The dataset consists of 11,054 website entries, each described by 30 features and a class label. The class label is either `1` (legitimate) or `-1` (phishing). The dataset is provided in both `.csv` and `.txt` formats. If using the `.txt` file, headers must be added manually. The features include website attributes such as the presence of an IP address in the URL, HTTPS usage, domain registration length, favicon usage, and many others—all of which contribute to the classification task.

## Methodology Used for Data Analysis
1. **Data Loading and Cleaning**: The dataset was loaded using pandas and checked for null or duplicate values.
2. **Exploratory Data Analysis (EDA)**: Distribution of class labels and individual feature contributions were visualized. Correlation heatmaps were used to identify the strongest predictors of phishing activity.
3. **Feature-Label Correlation**: Features most positively or negatively correlated with the class label were identified to understand their impact on the classification.
4. **Model Building**: A Random Forest Classifier was used to build the binary classification model. The dataset was split into training and testing sets in a 70:30 ratio.
5. **Model Evaluation**: Accuracy, precision, recall, and F1-score were used to evaluate performance.

## Correlation Analysis of Website Features
Features that had strong positive correlation with legitimate websites included `HTTPS`, `AnchorURL`, `WebsiteTraffic`, `PrefixSuffix-`, and `SubDomains`. These features typically indicate a trustworthy and well-maintained web presence.  
Conversely, features like `DomainRegLen`, `ShortURL`, `AbnormalURL`, and `Redirecting//` had high negative correlation with the class label, meaning they were more prevalent in phishing websites. These characteristics suggest a higher likelihood of malicious intent.  
Understanding these correlations is essential in building an accurate detection system, as they highlight which traits distinguish phishing websites from legitimate ones.

## Conclusions and Results
The final model achieved an accuracy of approximately **96%** using the Random Forest Classifier. It effectively distinguishes phishing websites based on URL structure, domain characteristics, and HTML attributes. The model performs well across all metrics—accuracy, precision, recall, and F1-score—indicating robustness.  
This project provides a solid foundation for deploying a phishing detection tool that can assist users and organizations in improving their cybersecurity posture.

---

