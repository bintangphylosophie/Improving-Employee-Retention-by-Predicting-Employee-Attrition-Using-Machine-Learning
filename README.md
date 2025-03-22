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
jupyter notebook All EDA and Insight.ipynb
jupyter notebook Preprocessing_merged.ipynb
jupyter notebook Modelling_Merged.ipynb

```
## Project Overview
Human resource (HR) is the key asset that needs effective management to helpcompanies achieve their business goals. In this project, we are faced with an issue related to human resources within a company. Our focus is to understand how retain employees to prevent the swelling of recrutmnt and training costs for new hires. By identifying factors causing employees to leave, we can promply address these concerns by creating relevant employee programs.

## Problem
Employee attrition threatens organizational stability, productivity, and long-term growth. Data indicates a sharp rise in resignations, particularly in 2018, alongside a declining trend in new hires. This imbalance underscores the need for proactive retention strategies to mitigate turnover.

Despite its high popularity, Fitbit faces challenges, particularly a lack of long-term user engagement. Data shows that 62% of users stop using it after 6-12 months, with the main reasons being boredom and the lack of personalized and relevant insights 
source: Statista(2023), Gartner(2022)

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


---
<br>

**Key steps in this stage include:**
## 1. Creating Column Target SatatusKerja
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

This is the next of the project, focusing on gaining insight 
<table>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/8a3562f1-4f19-489a-a2cf-c6d5ec13162d" width="300"></td>
    <td><img src="https://github.com/user-attachments/assets/e2592858-5f2c-44c4-a7f7-616c98959fbc" width="300"></td>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/c670b3e3-3530-4e59-8767-da16c0d851ab" width="300"></td>
    <td><img src="https://github.com/user-attachments/assets/ba8274cd-a33e-45fc-b108-b3a93962ca26" width="300"></td>
  </tr>
</table>









the modelling of the  dataset. The main goal of this stage is to build and evaluate models that can predict the target variable based on the preprocessed data. 🎯

The `Modelling_Merged.ipynb` notebook contains the modelling steps, where we build, train, and evaluate various machine learning models. This stage is crucial for finding the best model that can accurately predict the target variable. 📊

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
jupyter notebook Modelling_Merged.ipynb
```


**Key steps in this last stage include:**

## 1. **Models**: 🏗️<br>

Based on various studies, the models commonly used in calorie prediction include tree-based methods such as Random Forest and XGBoost, as well as linear models such as Linear Regression and Ridge Regression.
- Nipas et al. (2022) utilized Random Forest, Linear Regression, and Ridge Regression in their research.
- Reddy et al. (2023) also employed Linear Regression, Ridge Regression, and Random Forest Regression.
- Aziz et al. (2023) explored XGBoost, Linear Regression, SVM, and Random Forest, with the best results achieved using tree-based methods.

However, when our team tested the algorithm, we encountered a problem with overfitting. As a result, we experimented with other algorithms. A total of 13 algorithms were tested during the experiment, including:
- **Random Forest**
- **Linear Regression**
- **Ridge**
- **Lasso**
- **Elastic Net**
- **Decision Tree**
- **XGBoost**
- **Gradient Boosting**
- **Support Vector Regressor (SVR)**
- **Bayesian Ridge**
- **CatBoost Regressor**
- **LightGBM Regressor**
- **Extra Trees Regressor**

<br> 
In addition to experimenting with various algorithms, we also conducted multiple experiments on scaling, feature selection, and hyperparameter tuning using GridSearch for the algorithm with the best evaluation results.

**Scaling:** We compared two scaling methods, StandardScaler and RobustScaler.
Results: StandardScaler produced a smaller MAE compared to RobustScaler.

**Feature Selection:** We conducted experiments using feature elimination, testing several feature selection techniques-:
- Mutual Information Regression
- Correlation Analysis
- Feature Importance
- Particle Swarm Optimization (PSO)
Results: The Feature Importance technique yielded the lowest MAE and more balanced scores between the training and testing data.

**Tuning:** Hyperparameter tuning was performed only on the 3 best algorithms (those with the lowest MAE).

## 2. **Model Training and Evaluation**: 🏋️‍♀️🎯<br>
Model evaluation was performed using the MAE (Mean Absolute Error) metric, which was chosen for its robustness to outliers and its ability to provide a representative evaluation without disproportionately weighting large errors. A smaller MAE value indicates better model prediction accuracy.

From the evaluation results, the CatBoost model, **utilizing two features—'DistancePerStep' (total distance divided by total steps) and 'Total_MET'** (total daily energy calculated based on activity intensity)—produced the best prediction results with the lowest MAE compared to other models.

The following are the prediction results with the highest MAE:

### Model Results
| Model Name | MAE Train | MAE Test | MAE Dofferent |
|------------|--------------|-------------|-----------|
| CatBoost | 104.84 | 184.07 | 79.23 |
| LightGBM | 148.94 | 212.87 | 63.93 |
| Gradien Boosting | 146.01 | 204.92 | 58.91 |


We discovered that the catBoost Model with the lowest MAE test (184.07) and train (104.84), stability compared to other models. 

## 3. **Model Selection**: 🥇<br>

### Model Results
| Model Name |MAE Train | MAE Test | MAE Different |
|------------|--------------|-------------|-----------|
| CatBoost | **104.84** | **184.07** | **79.23** |

![image](https://github.com/user-attachments/assets/d23a70d6-6545-43a4-b316-5a9fd1779498)



## 🔑 Feature Importance 
Based on the CatBoost model Feature Importance:

![image](https://github.com/user-attachments/assets/569ee123-df91-48a0-a82b-5ab95f879428)

<br>

The importance feature are :
- 'DistancePerStep'
- 'Total_MET'

## 📝 Business Impact Simulation  
![Laporan Final Project - F4 pptx](https://github.com/user-attachments/assets/44b5eeae-29d7-40db-ae5c-5a9fc6d8e0dc)


**Explanation:** <br>
In this analysis, we simulate and assume that in month X, there will be 1,000 new users. Reviewing the previous data, we observe a decrease in active users to 62% of the total users, meaning that by month X+5, **before model only 380 active users remain** using the gadgets and applications.

According to Varecol, personalization in health applications can increase user participation by up to 30% of total users in the long term. With the implementation of personalization features and a **30% increase** in active users, the number of **active users in month X+5 after model is projected to reach 680.**

However, these results will need to be validated with new data after the machine learning model is deployed.


## ✅ Business Recommendation
### Feature Personalized ♥️
- **Personalized Daily/Weekly Calorie Targets**
To increase user flexibility in achieving daily/weekly calorie targets and increase user motivation in achieving goals. In accordance with goal-setting theory (Locke and Latham, 1990, 2022)
- **Deploy Model**
Deploy the best machine learning results, CatBoost with the 2 best features, in the cloud or on devices if possible.
If the predicted calorie burning results are still less than the daily target, the application will provide recommendations for activity adjustments to meet the weekly calorie burning target.

### Gamification 🎮 
- **Feature Challenge**
Gamification can be made into a challenge feature to motivate users to be more active in burning calories. 'Daily Challenge' such as the '10,000 Steps Challenge', and 'Leaderboard' to motivate users, because the majority are still classified as sedentary.

- **Feature Streak**
Then, the streak feature encourages users to stay active by providing rewards for each daily log or daily calorie target achievement.. This aims to maintain user retention and reduce boredom in using the application.

### Motivational Notification 🔔
- **Notification/Reminder**

We recommend the develover to create notification features to encourage users to use Fitbit more often and remind them of the best times to exercise, such as 7 am to 7 pm.


## Acknowledgements🌟

We would like to express our deepest appreciation to Rakamin Academy for providing the opportunity to work on this exciting project. The experience and knowledge we gained throughout this journey have been invaluable.

Special thanks to our mentor, Mr. Dino Febrianto, for his continuous guidance, patience, and support. His insights and wisdom have been instrumental in the successful completion of this project.

Finally, we would like to thank everyone who was involved in this project and those who provided their support and encouragement throughout our journey.

Regards, Bintang Phylosophie

<br>
<p align="center">
<img src="https://media1.giphy.com/media/3ohs7JG6cq7EWesFcQ/giphy.gif?cid=ecf05e47v1a2kre6ziee4vjvkc67vxhrwh8ho4089wc0aqli&ep=v1_gifs_search&rid=giphy.gif&ct=g" width="800">
</p>

🎓 This Final Project is a Rakamin Academy's program.
