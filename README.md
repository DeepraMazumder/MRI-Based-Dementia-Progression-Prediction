# MRI-Based-Dementia-Progression-Prediction

## Project Overview
The *MRI-Based-Dementia-Progression-Prediction* project aims to predict the progression of dementia in patients based on MRI data and other clinical features. It applies machine learning techniques, including **One-vs-Rest (OvR)** and **One-vs-One (OvO)** classifiers, particularly using **Support Vector Machines (SVM)**, to distinguish between three groups: *NonDemented*, *Demented*, and *Converted*. The project focuses on utilizing brain MRI imaging as a key input to predict if a patient will progress from mild cognitive impairment to dementia.

The dataset used for this project consists of longitudinal MRI data of 150 subjects, aged 60 to 96, with over 370 imaging sessions. These subjects include both non-demented and demented individuals, providing a comprehensive dataset for training and evaluation.

---

## Installation
To run the project locally, follow these steps:

1. Clone the repository:
   - `git clone https://github.com/your-username/MRI-Based-Dementia-Progression-Prediction.git`

2. Navigate to the project directory:
   - `cd MRI-Based-Dementia-Progression-Prediction`

3. Install the required dependencies:
   - `pip install --upgrade -r requirements.txt`

---

## Dataset
The dataset consists of the following key features:

- **Subject ID**: Unique identifier for each subject.
- **MRI ID**: Unique identifier for each MRI exam.
- **Group**: Target variable with three labels (*NonDemented*, *Demented*, *Converted*).
- **Visit**: Visit order.
- **MR Delay**: Time delay between MRI sessions.
- **M/F**: Gender (Male or Female).
- **MMSE**: Mini-Mental State Examination score (0–30).
- **CDR**: Clinical Dementia Rating (0–2).
- **eTIV**: Estimated total intracranial volume (mm³).
- **nWBV**: Normalized whole-brain volume (as a percentage).
- **ASF**: Atlas scaling factor.

---

## Exploratory Data Analysis (EDA)
The project explores the dataset through various visualizations and statistics:

- **Histogram Distributions**: Visualizes the distribution of key clinical features such as MMSE, CDR, and brain volumes.
- **Age Distribution**: Analyzes the age range of subjects.
- **Dementia Frequency**: Investigates the number of subjects diagnosed with dementia and their progression over time.
- **Correlation Heatmap**: Displays correlations between the clinical and MRI features.

---

## Pre-processing and Feature Engineering
- **Data Cleaning**: Removing unwanted columns, handling null values, and encoding categorical variables.
- **Feature Scaling**: Scaling MRI-derived volumes and clinical features.
- **Target Variable Encoding**: Encoding the group labels (*NonDemented*, *Demented*, *Converted*) for model training.

---

## Modeling

### **One-vs-Rest Classifier (OvR)**
The **One-vs-Rest** strategy was used for multi-label classification:

- Trained an OvR classifier with **SVM (Support Vector Machine)**.
- Evaluated the performance using **accuracy**, **precision**, **recall**, and **F1-score**.
- Computed the **ROC-AUC** for each class and visualized the ROC curve.

### **One-vs-One Classifier (OvO)**
The **One-vs-One** strategy was also applied to the dataset:

- Each class was paired with others to fit multiple classifiers, and predictions were aggregated to select the final class.
- Evaluated the model using a **confusion matrix** and **classification metrics**.

---

## **Results**
The project evaluated different classification strategies:

- **One-vs-Rest Classifier**:
  - **Accuracy**: XX%
  - **Precision**: XX%
  - **Recall**: XX%
  - **F1 Score**: XX%
  
- **One-vs-One Classifier**:
  - **Accuracy**: XX%
  - **Confusion Matrix**: Visualized using Seaborn
  
### Support Vectors
Identified the samples that served as support vectors for the SVM model, providing insight into the critical cases that define the decision boundaries between classes.

---

## Contributing
Contributions are welcome! If you'd like to contribute to the project, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a pull request.

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
