# Salifort-Motors-HR-Analytics-Project
Model to predict whether an employee will leave the company based on dataset variables 

## **Overview**
This project analyzes employee turnover at Salifort Motors, a fictional French-based alternative energy vehicle manufacturer. With a global workforce of over 100,000 employees, the company strives to support employee success and professional development. However, high turnover rates have prompted the leadership team to seek insights into the drivers of employee departure.

## **Objectives**

- Analyze employee data to uncover key factors driving turnover
- Build predictive models to forecast employee departure using:
    - Logistic Regression
    - Decision Tree
    - Random Forest
- Evaluate model performance and compare metrics to select the most effective approach.
- Provide actionable recommendations to the senior leadership team based on the findings.

## **Tools & Techniques**
- **Programming Language**: Python
- **Dev. Environment**: Google Colab
- **Libraries Used**:
  - Data Manipulation: pandas, numpy
  - Data Viz: matplotlib, seaborn
  - Machine Learning: scikit-learn
  

---

## **Dataset**
The dataset contains anonymized employee survey responses and organizational metrics such as:
- **Department**: Employee's department
- **Number of Projects**: Projects handled by the employee
- **Average Monthly Hours**:  Average working hours per month
- **Satisfaction Level**: Employee satisfaction rating
- **Last Evaluation**: Performance evaluation score
- **Work Accident**: Binary indicator of work accidents
- **Promotion in Last 5 Years**: Binary indicator of recent promotions
- **Left**: Binary target variable indicating whether an employee left the company

The data is stored in the `data/Dataset_HR_Project_Capstone.csv` file.

For more details, see the Data Dictionary provided in the repository.

## **Exploratory Data Analysis (EDA)**
Key insights from the EDA include:
- Correlation between satisfaction levels and employee departure.
- Impact of average monthly hours on turnover likelihood.
- Feature importance ranking from the Random Forest model.

Visualizations such as heatmaps, bar charts, and scatter plots were used to highlight these insights.

## **Machine Learning Models**
The project explores three models to predict employee turnover:
1. **Logistic Regression**
2. **Decision Tree**
3. **Random Forest**

These models are evaluated for their performance based on:
- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**
- **AUC-ROC Score**

The Random Forest model outperformed the Decision Tree in all evaluation metrics, demonstrating its ability to better generalize predictions on unseen data.

---

## **Key Results**

### **Logistic Regression**
Classification Report: 
![Logistic Regression Classification Report](logitstic_regression_.PNG)

The classification report above shows that the logistic regression model achieved a precision of 79%, recall of 82%, f1-score of 80% (all weighted averages), and accuracy of 82%. However, if it's most important to predict employees who leave, then the scores are significantly lower.

### **Model Comparison**
| Model              | Precision | Recall | F1-Score | Accuracy | AUC-ROC |
|---------------------|-----------|--------|----------|----------|---------|
| Decision Tree       | 0.9146    | 0.9169 | 0.9157   | 0.9719   | 0.9698  |
| Random Forest       | 0.9602    | 0.9156 | 0.9324   | 0.9787   | 0.9804  |

**Observations**:

- Random Forest Model:
    - Achieved the highest precision (0.9602) and accuracy (0.9787), making it the most effective at correctly identifying both classes.
  - The AUC-ROC score (0.9804) indicates that the Random Forest model is highly capable of distinguishing between employees likely to leave and those likely to stay.
    
- Decision Tree Model:
    - While performing well, its precision (0.9146) and accuracy (0.9719) are slightly lower than the Random Forest model.
    - The AUC-ROC score (0.9698) suggests strong performance but falls short of the Random Forest model.




### **Visualizations**



### **Insights**
- Employees in specific departments with high workloads (projects and hours) had higher turnover rates.
- Employee satisfaction and average monthly hours were significant predictors of departure.

---

## **How to Run the Project**
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Salifort-Motors-HR-Analytics-Project.git
