# Improving Employee Retention by Predicting Employee Attrition Using Machine Learning

<br>
<p align="center">
<img src="https://github.com/user-attachments/assets/84f95ee2-7d0f-4aa8-99c8-59c9968c64fd" width="500">
</p>
<br>
The dataset contains employee attrition information from  a fictional company from 2006 to 2020.

## 📚 Installation

This project requires Python and the following Python libraries installed:

- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scipy
- Sklearn

If you don't have Python installed yet, it's recommended that you install [the Anaconda distribution](https://www.anaconda.com/distribution/) of Python, which already has the above packages and more included.

To install the Python libraries, you can use pip:

```bash
pip install numpy pandas matplotlib seaborn scipy sklearn imbalanced-learn
```
To run the Jupyter notebook, you also need to have Jupyter installed. If you installed Python using Anaconda, you already have Jupyter installed. If not, you can install it using pip:
```bash
pip install jupyter
```

Once you have Python and the necessary libraries, you can run the project using Jupyter Notebook:
```bash
jupyter notebook Improving Employee Retention by Predicting Employee Attrition Using Machine Learning.ipynb
```
## Project Overview
Human resource (HR) is the key asset that needs effective management to helpcompanies achieve their business goals. In this project, we are faced with an issue related to human resources within a company. Our focus is to understand how retain employees to prevent the swelling of recrutmnt and training costs for new hires. By identifying factors causing employees to leave, we can promply address these concerns by creating relevant employee programs.

## Problem
Employee attrition threatens organizational stability, productivity, and long-term growth. Data indicates a sharp rise in resignations, particularly in 2018, alongside a declining trend in new hires. This imbalance underscores the need for proactive retention strategies to mitigate turnover.

## 🎯 Goals 
- Enhance Employee Retention: Strengthen strategies to retain employees and reduce turnover.
- Leverage Data for Decision-Making: Use historical employee data to gain insights into attrition trends.
- Implement Predictive Analytics: Develop models to anticipate resignations and enable proactive interventions.

## 🏁 Obective 
Analyze Employee Data: Examine historical trends, employee attributes, and resignation patterns to uncover key drivers of turnover.
Generate Actionable Insights: Identify factors influencing retention and recommend strategies for improvement.
Develop Predictive Models: Create data-driven models to forecast resignations and help the company address employee concerns proactively.


The process will go through the following steps to achieve the objectives:
1. Data Understanding
2. Data Preprocessing
3. Feature Engineering
4. Insight
5. Exploratory Data Analysis
6. Data Preparation
7. Machine Learning
<br>
<br>

# 🔎Stage 1: Data Understanding and Preprocessing 

<br>
<p align="center">
<img src="https://user-images.githubusercontent.com/74038190/212749726-d36b8253-74bb-4509-870d-e29ed3b8ff4a.gif" width="500">
</p>
<br>

## 📊 About Dataset 

### 📋Dataset consist :
- There are 287 rows and 25 columns in the dataset. 
- The target column in this dataset is `StatusKerja` has extracted from `TanggalResign`
- The dataset contains several missing values, which are filled considering the number of missing values, their skewness, and the data type
- The dataset does not have duplicated data
- The dataset does not have outliers
- Several inconsistent data values have been tidied up.


### 📝Features

| Feature | Explanation |
|---------|-------------|
| Username| Unique employee username|
| EnterpriseID| ID within the enterprisek|
| StatusPernikahan| Marital status |
| JenisKelamin | Gender|
| StatusKepegawaian | Employment status |
| Pekerjaan |  Job position |
| JenjangKarir | Career level |
| PerformancePegawai | PerformancePegawai |
| AsalDaerah | Region of origin |
| HiringPlatform | Platform used for hiring |
| SkorSurveyEngagement | Engagement score |
| SkorKepuasanPegawai | Employee satisfaction score |
| JumlahKeikutsertaanProjek | Number of projects participated in |
| JumlahKeterlambatanSebulanTerakhir | Recent monthly delay count |
| JumlahKetidakhadiran | Absence count |
| NomorHP | Employee's phone number |
| Email | Employee's email address |
| TingkatPendidikan | Educational level |
| PernahBekerja | Previous employment history |
| IkutProgramLOP | Participation in a specific program (LOP) |
| AlasanResign | Reason for resignation (if applicable) |
| TanggalLahir | Date of birth |
| TanggalHiring | Date of hiring |
| TanggalPenilaianKaryawan | Date of employee evaluation |
| TanggalResign | Date of resignation for resigned employees |

<br>
<br>



# ⚙️ Stage 2: Feature Engineering

<br>
<p align="center">
<img src="https://user-images.githubusercontent.com/74038190/221352995-5ac18bdf-1a19-4f99-bbb6-77559b220470.gif" width="400">
</p>


This is the second stage of  focusing on feature engineering of the dataset. The main goal of this stage is to clean and transform the raw data to make it suitable for data analysis. 🧹🔄

<br>

**Key steps in this stage include:**
## 1. Creating Column Target: SatatusKerja
I create the column StatusKerja to serve as our label by defining 'Tidak Bekerja' for rows with a non-null value in `TanggalResign` (indicating resignation) and 'Masih Bekerja' for rows with a null value in `TanggalResign` (indicating active employment). And the other things are adjusting datatype and some feature extraction.

## 2. Column: Hiring
- Tanggal hiring
- Tanggal resign
- Tahun hiring
- Bulan hiring
- Hari hiring
## 3. Column: UmurKaryawan
- Usia karyawan
- Kategori usia
## 4. Column: DurasiBekerja
- Tanggal penilaian karyawan
- Tanggal hiring
- Lama menjabat

<br>
<br>

# 🚀 Stage 3: Insight

<br>
<p align="center">
<img src="https://media0.giphy.com/media/Y4PkFXkfTeEKqGBBsC/giphy.gif?cid=ecf05e47numetagrmbl2rxf6x0lpcjgq1s340dfdh1oi0x9w&ep=v1_gifs_related&rid=giphy.gif&ct=g" width="420">
</p>

This is the next phase of the project, focusing on gaining insights. Here are some valuable insights derived from the dataset
<div align="center">
  <table>
    <tr>
      <td><img src="https://github.com/user-attachments/assets/8a3562f1-4f19-489a-a2cf-c6d5ec13162d" width="300"></td>
      <td><img src="https://github.com/user-attachments/assets/e2592858-5f2c-44c4-a7f7-616c98959fbc" width="300"></td>
    </tr>
    <tr>
      <td><img src="https://github.com/user-attachments/assets/c670b3e3-3530-4e59-8767-da16c0d851ab" width="300"></td>
      <td><img src="https://github.com/user-attachments/assets/ba8274cd-a33e-45fc-b108-b3a93962ca26" width="300"></td>
    </tr>
    <tr>
      <td><img src="https://github.com/user-attachments/assets/a3d3fdd9-be1d-4442-affd-38f5baa5e7d5" width="300"></td>
      <td><img src="https://github.com/user-attachments/assets/a95ba87f-b09d-4556-b8d2-3e65f8364202" width="300"></td>
    </tr>
  </table>
</div>
For further and deeper analysis and explanation, kindly check:

[Improving Employee Retention (PDF)](https://github.com/bintangphylosophie/Improving-Employee-Retention-by-Predicting-Employee-Attrition-Using-Machine-Learning/blob/main/Improving%20Employee%20Retention%20by%20Predicting%20Employee%20Attrition%20Using%20Machine%20Learning.pdf)



# ⚙️ Stage 4: Data Preprocessing
This stage is focusing on data preprocessing of the dataset transform the data to make it suitable for modeling
## 1. **Feature Encoding** 🏷️<br>
I encode all of our categorical features (strings) using the label encoding method. All features have been encoded at the feature extraction stage, given that our features are ordinal data and the majority of machine learning algorithms perform better with numerical data.

## 2. **Data Scaling** 🏷️<br>
Data scaling is the process of transforming feature values within a dataset to ensure they have a uniform range. I performed using MinMaxScaler to improve machine learning algorithm performance that will be perform in next stage.

## 3. **Feature Selection** 🎯<br>
Since I am working with categorical features and a classification problem, SelectKBest with chi2 is a great choice because it is: fast, helps remove irrelevant features, works well with encoded categorical data. This method is commonly used to reduce dimensionality by keeping only the most relevant features for predictive modeling. I only keep top 15 features.

## 4. **Data Splitting**<br>
Data splitting is the process of dividing a dataset into different subsets to train, validate, and test a machine learning model. 
The main goal of this stage is to build and evaluate models that can predict the target variable based on the preprocessed data. The data splitted into 20% train and 80% test.


Prior to this, the dataset was split into training and testing sets. After completing all preprocessing steps, the data is clean and ready for machine learning to predict the target.🤖

<br>
<br>


# 🚀 Stage 5: Modelling
<br>
<p align="center">
<img src="https://media0.giphy.com/media/Y4PkFXkfTeEKqGBBsC/giphy.gif?cid=ecf05e47numetagrmbl2rxf6x0lpcjgq1s340dfdh1oi0x9w&ep=v1_gifs_related&rid=giphy.gif&ct=g" width="420">
</p>
The main goal of this stage is to build and evaluate models that can predict the target variable based on the preprocessed data. 🎯

## 📚 Installation

This project requires Python and the following Python libraries installed:

- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scipy
- Sklearn
- shap

If you don't have Python installed yet, it's recommended that you install [the Anaconda distribution](https://www.anaconda.com/distribution/) of Python, which already has the above packages and more included.

To install the Python libraries, you can use pip:

```bash
pip install numpy pandas matplotlib seaborn scipy sklearn imbalanced-learn xgboost shap
```
To run the Jupyter notebook, you also need to have Jupyter installed. If you installed Python using Anaconda, you already have Jupyter installed. If not, you can install it using pip:
```bash
pip install jupyter
```

Once you have Python and the necessary libraries, you can run the project using Jupyter Notebook:
```bash
jupyter notebook Improving Employee Retention by Predicting Employee Attrition Using Machine Learning.ipynb
```


**Key steps in this last stage include:**

## 1. **Models**: 🏗️<br>

I experimented with other algorithms. A total of 5 algorithms were tested during the experiment, including:
- **Support Vector Machine**
- **Gradient Boosting**
- **Decision Tree**
- **Random Forest**
- **Logistic Regression**

<br> 

**Tuning:** Hyperparameter tuning was performed only on the 1 best algorithms (those with the highest ROC AUC score).

## 2. **Model Training and Evaluation**: 🏋️‍♀️🎯<br>

The following are the prediction results with the highest Accurcy and ROC-AUC:

### Model Results
| Model Name | Accuracy | ROC AUC | 
|------------|--------------|-------------|
| Support Vector Machine | 0.67 | 0.50 | 
| Gradient Boosting | 0.94 | 0.94 | 
| Decision Tree | 0.93 | 0.93 | 
| Random Forest | 0.89 | 0.85 | 
| Logistic Regression | 0.70 | 0.57 | 


We discovered that the Gradient Boosting Model with the highest Accuracy (0.94) and ROC AUC (0.94), stability compared to other models. 

## 3. **Model Selection**: 🥇<br>

### Model Results
| Model Name | Accuracy | ROC AUC | 
|------------|--------------|-------------|
| Gradient Boosting | **0.94** | **0.94** |

with confussion matrich and ROC AUC score like this:

<div align="center">
  <table>
    <tr>
      <td><img src="https://github.com/user-attachments/assets/259784b2-2b39-4912-b555-26b4d56dfdeb" width="400"></td>
      <td><img src="https://github.com/user-attachments/assets/ffb76db3-751f-4ef9-b82a-56c05b3ec943" width="400"></td>
    </tr>
  </table>
</div>

## 🔑 Feature Importance 
Based on the Gradient Boosting model Feature Importance:

<div align="center">
  <img src="https://github.com/user-attachments/assets/200d233e-1cdc-403e-bb6a-8887b523f375" width="400">
</div>

<br>

The top importance feature with score > 0.01 are :
- `AlasanResign`
- `AsalDaerah_JakartaSelatan`
- `UsiaKaryawan`
- `HiringPlatform_Diversity_Jobfair`


## ✅ Business Recommendation
To improve retention, the company deploys a machine learning model to identify key factors leading to resignations. with AI-driven insights, the company designs targeted retention strategies:

### The model strongly relies on "AlasanResign" (Resignation Reason), meaning that resignation trends must be analyzed deeply to take proactive action. Since working hour is the dominant factor, some action recommend:
- **Analyze Overtime Trends:** Check which departments consistently work overtime and why.
- **Survey Employees:** Get feedback on workload, stress levels, and preferred work hours.
- **Compare Productivity Metrics:** Measure performance vs. hours worked to find the optimal balance.
- **Implement Flexible Working Hours:** Allow employees to choose a start time (e.g., 7 AM - 3 PM, 9 AM - 5 PM, 11 AM - 7 PM)
- **Implement Hybrid & Remote Work Options:** Allow employees to work 2-3 days from home per week.
- **Reduce Unnecessary Meetings & Improve Time Efficiency:** Limit Meetings to 30-45 Minutes, Set "No-Meeting Days“,Block 1-2 days per week for deep work without interruptions.

### The model detects that employees from Jakarta Selatan and mid-employees have a higher risk of resigning. 
- **Personalized Exit Interviews:** Focus on  mid-employee and Jakarta Selatan employees to understand their concerns, "Stay Interviews": Monthly check-ins with at-risk employees
- **Internal Mentorship Programs:** Pair mid-level employees with senior mentors.

#### Machine learning provided valuable insights, but human intervention was key in designing effective retention strategies. XYZ Corp launches AI-powered retention programs for 6 months and tracks the impact.

## 📝 Business Impact Simulation  
Company Name Profile: **XYZ Corp**
A tech company, XYZ Corp, has been struggling with high employee turnover, affecting productivity, morale, and recruitment costs. To improve retention, the company deploys a machine learning model to identify key factors leading to resignations. with AI-driven insights, the company designs targeted retention strategies.

<div align="center">
  <img src="https://github.com/user-attachments/assets/78c8ecef-dbf8-444e-9c8c-4906da6ebf09" width="600">
</div>


## Acknowledgements🌟

I would like to express our deepest appreciation to Rakamin Academy for providing the opportunity to work on this exciting project. The experience and knowledge we gained throughout this journey have been invaluable.

Finally, I would like to thank those who provided their support and encouragement throughout my journey.

Regards, Bintang Phylosophie

<br>
<p align="center">
<img src="https://media1.giphy.com/media/3ohs7JG6cq7EWesFcQ/giphy.gif?cid=ecf05e47v1a2kre6ziee4vjvkc67vxhrwh8ho4089wc0aqli&ep=v1_gifs_search&rid=giphy.gif&ct=g" width="800">
</p>


