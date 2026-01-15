##Consumer Complaint Classification



## 📝  Description

[cite_start]The objective of this task is to perform text classification on the [Consumer Complaint Database](https://catalog.data.gov/dataset/consumer-complaint-database)[cite: 111]. [cite_start]The goal is to categorize consumer complaint narratives into one of the following four product categories[cite: 112]:

* Credit reporting, repair, or other
* Debt collection
* Consumer Loan
* Mortgage

[cite_start]The project adheres to the required steps including data analysis, pre-processing, model selection, comparison, evaluation, and prediction[cite: 113].

## 🚀 How to Run the Code

This project was developed in a Kaggle Notebook environment. To replicate the results, please follow these steps:

1.  **Environment**: Use a Kaggle Notebook or a similar Jupyter environment with standard data science libraries (Pandas, Scikit-learn, NLTK, Seaborn) installed.
2.  **Dataset**: Download the `complaints.csv` file from the official source and upload it to the notebook's input directory. The code expects the file to be at the path `/kaggle/input/complaints/complaints.csv`.
3.  **Execution**: Open the notebook (`.ipynb` file) and run all cells sequentially from top to bottom. The notebook is self-contained and will handle all data processing, model training, and evaluation.

## 🛠️ Project Workflow

The project was executed following the exact steps outlined in the assessment document:

1.  **Explanatory Data Analysis (EDA)**: The initial dataset of over 11 million rows was loaded and analyzed. [cite_start]We identified a large number of missing values in the `Consumer complaint narrative` column and a class imbalance in the target `Product` column[cite: 114].
2.  [cite_start]**Text Pre-Processing**: To prepare the data for modeling, we performed several key steps: dropped rows with no narrative, consolidated product categories, created a balanced sample of 9,461 complaints per category, and cleaned the text by converting to lowercase, removing punctuation/stopwords, and applying lemmatization[cite: 117].
3.  [cite_start]**Model Selection**: A **Multinomial Naive Bayes** model was selected as a strong baseline for text classification[cite: 119].
4.  [cite_start]**Model Comparison**: To improve upon the baseline, a **Linear Support Vector Machine (SVM)** model was also trained and evaluated on the same data[cite: 120].
5.  **Model Evaluation**: Both models were evaluated using Accuracy, Precision, Recall, F1-Score, and a Confusion Matrix. [cite_start]The Linear SVM was identified as the superior model[cite: 121].
6.  [cite_start]**Prediction**: A final step demonstrated how to use the trained SVM model to predict the category of a new, unseen complaint narrative[cite: 122].

## 📊 Results and Screenshots

The Linear SVM model outperformed the Multinomial Naive Bayes model across all metrics, making it the final selected model.

### Model Performance Comparison

| Model | Overall Accuracy |
| :--- | :--- |
| Multinomial Naive Bayes | 85.1% |
| **Linear SVM** | **87.95%** |

---

### Screenshot 1: Final Model Evaluation

<img width="1919" height="976" alt="image" src="https://github.com/user-attachments/assets/93ea614e-ae66-4db8-93f8-1e46bfab0f0f" />

<img width="1839" height="855" alt="image" src="https://github.com/user-attachments/assets/72333df1-9408-4615-9e6c-7868090b359b" />



---

### Screenshot 2: Prediction on New Data

<img width="1919" height="970" alt="image" src="https://github.com/user-attachments/assets/f6bdddfe-89bd-44d0-9535-f6974bcbe817" />
