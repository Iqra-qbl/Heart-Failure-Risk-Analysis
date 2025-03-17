# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

# Heart Failure Risk Analysis

** This project utilizes data-driven insights to identify key risk factors and predictors of heart failure, enabling early diagnosis and preventive care. The tool supports multiple data formats and provides an intuitive interface for both novice and expert data scientists, medical practitioners, WHO and other stakeholders.


## Dataset Content
* **Dataset:** `heart_dataset.csv` (https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)
- **Dataset Source:** This dataset was created by combining different datasets already available independently but not combined before. In this dataset, 5 heart datasets were combined over 11 common features which makes it the largest heart disease dataset available so far for research purposes. The five datasets used for its curation were: Cleveland (303 observations), Hungarian (294 observations), Switzerland (123 observations), Long Beach VA (200 observations) and Stalog (Heart) Data Set (270 observations). Total 1190 observations with 272 duplicated observations. Final dataset had **918** observation rows and **12** feature columns.
- **Columns of Interest:**
  - **Demographics:** Age, Sex
  - **Medical Indicators:** ChestPainType, RestingBP, FastingBS, Cholesterol, RestingECG, MaxHR, ExerciseAngina
  - **Column Feature Information:**
    - Age: age of the patient [years]
    - Sex: sex of the patient [M: Male, F: Female]
    - ChestPainType: chest pain type [TA: Typical Angina, ATA: Atypical Angina, NAP: Non-Anginal Pain, ASY: Asymptomatic]
    - RestingBP: resting blood pressure [mm Hg]
    - Cholesterol: serum cholesterol [mm/dl]
    - FastingBS: fasting blood sugar [1: if FastingBS > 120 mg/dl, 0: otherwise]
    - RestingECG: resting electrocardiogram results [Normal: Normal, ST: having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV), LVH: showing probable or definite left ventricular hypertrophy by Estes' criteria]
    - MaxHR: maximum heart rate achieved [Numeric value between 60 and 202]
    - ExerciseAngina: exercise-induced angina [Y: Yes, N: No]
    - Oldpeak: oldpeak = ST [Numeric value measured in depression]
    - ST_Slope: the slope of the peak exercise ST segment [Up: upsloping, Flat: flat, Down: downsloping]
    - HeartDisease: output class [1: heart disease, 0: Normal]


## Healthcare Requirements
 1. Identify Key Risk Factors for Heart Failure: Use the dataset to highlight the most significant predictors of heart failure. For example, assess the roles of demographics like age and gender, and medical indicators such as cholesterol levels and blood pressure.

 2. Develop a Predictive Model: Create a machine learning model to predict the likelihood of heart failure for patients based on their clinical features, aiding healthcare professionals in early diagnosis and preventive measures.

 3. Visualize Relationships and Insights for medical practictioners and non-tech people.


## Hypothesis and how it was validated?
  1. Age and gender as Predictors
      Hypothesis: Individuals aged 60 and above are at significantly higher risk of heart failure compared to younger individuals and males are more likely to experience heart failure than females.

      Validation: Analysis and bar chart to show distribution of heart failure risk across demographics with target variable. 
   
   2. Cholesterol Levels
      Hypothesis: High levels of cholesterol (represented by Cholesterol) are positively associated with an increased risk of heart failure.
      
      Validation: Correlation analysis and matrix for numerical variables (e.g., Cholesterol vs. RestingBP).

   3. Blood Pressure
      Hypothesis: Patients with higher blood pressure are at greater risk of developing heart failure than those with normal blood pressure levels.
      Validation: Correlationship heatmap and scatter plot show the link between high resting blood pressure and heart disease, in dashboard the bar chart also shows the higher resting blood pressure the higher risk of heart failure.

   4. Combination of Factors
     Hypothesis: The presence of two or more risk factors and elevation of medical indicators (e.g., ECG, High_BP, Excercide Angina, Maximum heart rate) dramatically increases the probability of heart failure compared to isolated risk factors.

     Validation:   Pair plots to observe relationships between multiple numerical features at once.


## Project Plan
1. **Data Acquisition and Understanding**
   
   Step 1.1: Collect the dataset heart_dataset.csv from Kaggle.
   Step 1.2: Review the dataset structure, source, and features (demographics, medical indicators, and target variable HeartDisease).
   Step 1.3: Understand the dataset's context.

2. **Data Preprocessing**
   
   Step 2.1: Address duplicate rows by checking for duplicated observations.
   Step 2.2: Handle missing values, ensuring the dataset is clean and complete for analysis.
   Step 2.3: Identify outliers using skewness and kurtosis analyses for numerical features (e.g., FastingBS, Oldpeak).
   Step 2.4: Normalize and scale features as needed (e.g., using StandardScaler for consistent input to predictive models).

3. **Exploratory Data Analysis (EDA)**
   
   Step 3.1: Conduct univariate analysis:
   - Analyze the distribution of key features like age, gender, cholesterol levels, and maximum heart rate.
   - Identify trends, such as the prevalence of heart disease in older age groups and males.
   Step 3.2: Perform bivariate and multivariate analyses:
   - Analyze correlations between features (e.g., resting blood pressure, cholesterol, and heart disease risk).
   - Create visualizations such as scatter plots, box plots, and correlation heatmaps.
   Step 3.3: Conduct statistical tests, such as chi-square, to validate relationships between categorical features and heart disease.

4. **Feature Engineering**
   
   Step 4.1: Create new features or refine existing ones, such as grouping ages into categories or combining multiple risk indicators.
   Step 4.2: Reduce dimensionality using PCA to highlight significant patterns and simplify data for predictive modeling.

5. **Predictive Modeling**
   
   Step 5.1: Split data into training and testing sets using train_test_split.
   Step 5.2: Develop predictive models using algorithms such as:
   - Logistic Regression
   - Decision Trees
   - Random Forest
   - XGBoost
   Step 5.3: Evaluate model performance with metrics including:
   - Accuracy, precision, recall, and F1-score.
   - AUC-ROC curves to assess the trade-off between sensitivity and specificity.

6. **Data Visualization and Insights**
   
   Step 6.1: Create visualizations to address business requirements:
   - Age distribution, gender distribution, and chest pain type bar charts.
   - Scatter plots for resting blood pressure and regression lines for trends.
   - PCA cluster plots and confusion matrices for model evaluation.
   Step 6.2: Develop a dashboard wireframe
   Step 6.3: Develop an interactive Power BI dashboard to consolidate findings and allow stakeholders to explore insights.

7. **Reporting and Presentation**
   
   Step 7.1: Summarize the analysis, key findings, and predictive model performance in a final report.
   Step 7.2: Provide actionable recommendations to healthcare stakeholders, such as focusing interventions on high-risk groups (older males with high cholesterol or blood pressure).

8. **Ethical Considerations**
   
   Step 8.1: Ensure no personal identifiable information is included, maintaining patient anonymity.
   Step 8.2: Address potential biases due to the dataset's imbalance (79% male patients) and document mitigation strategies (e.g., chi-square test validation).

This project plan ensured that the analysis was systematic, transparent, and aligned with the project's objectives of identifying risk factors, supporting predictive models, and providing meaningful visualizations for healthcare interventions.


## The rationale to map the business requirements to the Data Visualisations

1. Identifying key risk factors for Heart Failure by understanding demographic and clinical factors that contribute to heart failure
 
Visualizations Used: Bar charts, pie charts, scatter plots, and box plots to explore demographic and clinical features in relation to heart failure.

Key Findings from Visualizations:

 - The age distribution plot shows that the majority of patients fall between 40 and 70 years old, with a peak around 60 years, indicating heart failure is more prevalent in older age groups.

 - The gender distribution chart reveals a higher prevalence of heart disease in males than females, aligning with existing medical research.

 - The chest pain type bar chart indicates that asymptomatic chest pain ('ASY') is the most common type among patients with heart disease, emphasizing the importance of regular check-ups for asymptomatic individuals.

 - The scatter plot for resting blood pressure shows a positive correlation with age, stressing the need for blood pressure management, particularly for older adults.

 - The box plot for cholesterol levels highlights wide variability, with some patients having extremely high cholesterol, emphasizing the importance of monitoring cholesterol.

2. Develop and support predictive modeling to build machine learning models to predict the likelihood of heart failure and assess their performance
 
Visualizations Used: Line plots to illustrate trends like maximum heart rate changes and scatter plots with regression lines to identify other notable relationships (e.g., maximum heart rate versus heart disease occurrence).
 
Key Findings from Visualizations:

 - The PCA cluster plot highlights distinct patterns between patients with and without heart disease, providing insights into separable groups that can enhance predictive modeling.

 - Visualizations Used: PCA cluster plots to visualize data separation, ROC curves to evaluate model performance, and confusion matrices to visualize classification accuracy and misclassification rates.

3. Gain Deeper Insights Through Data Exploration to Explore trends and patterns to provide actionable insights for stakeholders.

Key Findings from Visualizations:

The maximum heart rate line plot shows that patients with heart disease tend to have lower maximum heart rates, suggesting reduced exercise capacity as a potential indicator of heart disease.


## Analysis techniques used & key findings
  1. Conducted a Exploratory data analysis (EDA) to gain an initial understanding of the dataset such as basic by checking general information regarding the data such as column names, datatypes of columns, number of entries and the memory space used, duplicate or missing values. Followed by skewness and kurtosis analyses for numerical features to find outliers: 
  
  - Most features were close to normal distribution but FastingBS and Oldpeak werre right-skewed, suggesting outliers
  - RestingBP was slightly peaked, meaning some extreme values exist
  - HeartDisease has a very flat distribution, indicating balanced cases    
  - The outlier were all replaced with medians except for FastingBS & HeartDisease columns as they were binary and would become distorted if changed

 2. Then conducted Univariate Analysis for Categorical Features, finding that:

- Males have a higher prevalence of heart disease
- ASY (Asymptomatic) chest pain type is a strong indicator of heart disease
- ST-T wave abnormality in ECG is associated with heart disease
- Exercise-induced angina is a significant risk factor (85.2% with heart disease)

 3. Followed by a Chi-Square Test to check for data bias, finding that:

- Males **(79%)** dominate the dataset, while females make up only **21%**
- Heart disease is more prevalent in **males (63.2%)** compared to **females (25.9%)**
- Females are more likely to be free from heart disease **(74.1%)** than males **(36.8%)**
- The largest age group is **50-59 years (40.7%)**, followed by **60-69 years (24.2%)** and **40-49 years (22.9%)**
- Very few individuals are under 30 years (0.4%) or over 70 years (3.3%)- Heart disease risk increases with age, especially for men
- Women are at lower risk overall but see an increase in their 60s
- Sex, ChestPainType,RestingECG and HeartDisease have statistical significance to 'Heart Disease' 
- The association between gender, age, and heart disease is highly significant (not due to random chance)

4. Then conducted a Correlation Matrix, which showed that:

- A higher Oldpeak value has strong positive correlation and is strongly associated with a higher likelihood of heart disease
- Higher fasting blood sugar levels are moderately associated with heart disease
- Higher resting blood pressure shows a moderate positive correlation with heart disease
- Higher maximum heart rate achieved during exercise is strongly associated with a lower likelihood of heart disease
- Age shows a weak positive correlation with heart disease
- Cholesterol levels show a weak positive correlation with heart disease


## Dashboard Design

![Full Dashboard Design](https://github.com/Iqra-qbl/Heart-Failure-Risk-Analysis/blob/main/Outputs/Visuals/Dashboard%20Design.png)

* There is only one interactive dashboard page in PowerBI. 
* It has a large red and blue heart image to represent what the main topic of the dashboard is which is heart failure analysis. 
* To prove the age and gender as predictors hypothesis, created demographic bar charts to compare risk score for different age groups and genders. 
* Created a pie chart to highlight the number of patients at risk and what their respective risk level was based on high, medium, normal and low risk category.
* Created multiple option selection options for Risk level and Chest Pain Type to get relevant figures and analysis.

![Dashboard top](https://github.com/Iqra-qbl/Heart-Failure-Risk-Analysis/blob/main/Outputs/Visuals/Dashboard%20Design%20Screenshot.png)

* Created a place card for average cholestrol and mutliple line charts and bar charts to compare distribution of values in other main medical indators in dataset.
* Created line chart to showcase average maximum heart rate and forecast
* Added decomposition tree to analyse Average Risk score and drilling down into the key drivers behind the metric, such as understanding factors contributing to heart failure risk predictions using features such as gender, age groups, heart disease, chest pain type, resting ECG, resting blood pressure, mamixmum heart rate and st slope values.

![Dashboard middle](https://github.com/Iqra-qbl/Heart-Failure-Risk-Analysis/blob/main/Outputs/Visuals/Dashboard%20Design%20Screenshot2.png)

* Wanted to create scatter plots like the pair plots in data visualisation section but couldn't compute how to recreate them in an interactive way in PowerBI dashboard and had to troubleshoot and justify whether they were important to be included just to create graph diversity.

* How were data insights communicated to technical and non-technical audiences?

I am not a medical expert but used Copliot AI to highlight which features would be suitable for dashboard for medical practioners and common layman.

* Explain how the dashboard was designed to communicate complex data insights to different audiences. 
Created a blue and red palette that conveys the medical them, kept the graphs clean and uncomplicated for ease of use and encourage experimentation by technical and non-technical people. Also dedicated a section in dashboard to explain how to use the dashboard and see different analyses.


## Unfixed Bugs
* There are no unfixed bugs.

* Did you recognise gaps in your knowledge, and how did you address them?
Yes, I would take a break, research and then troubleshoot with Copilot and ChatGPT AI about what I exactly wanted the code to do and produce and would try different commands to get the exact code and outlook I wanted. 

* If applicable, include evidence of feedback received (from peers or instructors) and how it improved your approach or understanding.


## Development Roadmap
* What challenges did you face, and what strategies were used to overcome these challenges?
I spent lot of time on creating plots and graphs in data visualisation jupyter notebook and struggled to recreate them in PowerBI, I even exported all the visuals created using plotly as html files with the intent to create a Tableau dashboard instead but dropped that idea as I already had a dashboard halfway done in PowerBI and tried to create the possibly relevant graphs for a non-technical person in a PowerBI dashboard.

Another time-consuming challenge I faced was that I spent more than two days creating different predictive models, finally selecting Logistics Regression Model (LRM) for its better Recall result and wanted to predict risk score and risk level for the whole dataset and export it into two new columns in dataframe and export that into a new csv file but there was some variable mixup that only the trained dataset chunk was being exported. Fixed the code by meticulously going through the predictive modelling with Copilot AI to spot and fix the issue.  

* What new skills or tools do you plan to learn next based on your project experience? 

I would like to explore Streamlit and Heroku a bit more in the future to create independent dashboards. I will also conduct some experiments to create dashboards in Plotly Dash and Tableau for practice.


## Inputs
- The original `heart_dataset` was saved in Inputs folder.
- AI generated hypothesis ideation and project plan for data analysis was saved in Inputs folder.
- The cleaned and transformed dataset produced in ETL notebook was saved in Inputs folder as an input for Data Visualisation notebook.
- Dashboard wireframe was saved in Inputs folder.


## Outputs

- The two csvs: one to clean and transform the heart dataset produced in ETL notebook and another csv, including the predicted risk score and risk levels columns, were exported in Outputs folder.
- PowerBI dashboard main file was saved in Outputs folder.
- Screenshots and many of the data visualisations were saved as html in Outputs/Visuals folder.

## Jupyter Notebooks
- The `ETL`, `Data visualisation` and `Predictive Modelling` sections were divided into their respective jupyter notebooks in `jupyter_notebooks` folder.

## Main Data Analysis Libraries

* NumPy: Efficient numerical computations and array manipulation, used in predictive modelling to round up Risk score percentage.
* Pandas: Data manipulation and analysis using dataframes, used in importing and exporting csv datasets files into dataframes for analysis in ETL jupyter notebook. 
* Matplotlib: Plotting and data visualization, used to create separate histograms for each numerical feature in dataset. 
* Seaborn: Advanced and aesthetically pleasing statistical plots, used to create heatmap correlation in data visualisation section.
* Plotly: Easy interactive visualizations, used to create most of the graphs and charts in data visualisation section. 
* Scipy (Stats): Scientific computations including statistical tests, used to carry out chi-square test analysis in ETL section.
* Scikit-learn (PCA, StandardScaler, train_test_split, LogisticRegression, Metrics, Decision Trees, KNeighborsClassifier ): used in predictive modelling to build, evaluate, and optimize predictive models to predict heart failure risk.
* XGBoost: High-performance gradient-boosted decision trees, used in predictive modelling to create a XGBoost model to predict heart failure risk.
* Warnings: Suppress warnings for cleaner output, there were many warnings in predictive modelling and this library was used to make the output cleaner.

## Credits 

* fedesoriano. (September 2021). Heart Failure Prediction Dataset. Retrieved [Date Retrieved] from https://www.kaggle.com/fedesoriano/heart-failure-prediction.
* Inspired by https://www.kaggle.com/code/tanmay111999/heart-failure-prediction-cv-score-90-5-models/notebook

### Content & Media

- Most of the code, ideation, design thinking and code optimisation was developed with the assistance of Copilot and ChatGPT AIs
- The Code Institute logo is from (https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)
- The heart image was generate by using Copilot
- The dashboard wireframe was made in Balsamic Wireframes app
- Rest of the diagrams are exported from the project's Data Visualisations jupyter notebook

## Acknowledgements
* Thanks to Vasi and Niel and my incredibly talented peers in my cohort for providing motivation throughout this project.