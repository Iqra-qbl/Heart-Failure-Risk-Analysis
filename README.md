# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

# Heart Failure Risk Analysis

**Project XYZ** is a comprehensive data analysis tool designed to streamline data exploration, analysis, and visualisation. The tool supports multiple data formats and provides an intuitive interface for both novice and expert data scientists.


## Dataset Content
* Describe your dataset. Choose a dataset of reasonable size to avoid exceeding the repository's maximum size of 100Gb.


## Business Requirements
* Describe your business requirements


## Hypothesis and how it was validated?
* 1. Age and gender as a Predictor
      Hypothesis: Individuals aged 60 and above are at significantly higher risk of heart failure compared to younger individuals and males are more likely to experience heart failure than females.

      Validation: Analysis and bar chart to show distribution of heart failure risk across demographics with target variable. 
   
   3. Cholesterol Levels
      Hypothesis: High levels of cholesterol (represented by Cholesterol) are positively associated with an increased risk of heart failure.
      
      Validation: Correlation analysis and matrix for numerical variables (e.g., Cholesterol vs. RestingBP).

   4. Blood Pressure
      Hypothesis: Patients with higher blood pressure are at greater risk of developing heart failure than those with normal blood pressure levels.

  5. Combination of Factors
     Hypothesis: The presence of two or more risk factors and elevation of medical indicators (e.g., ECG, High_BP, Excercide Angina, Maximum heart rate)
     dramatically increases the probability of heart failure compared to isolated risk factors.

## Project Plan
* Outline the high-level steps taken for the analysis.
* How was the data managed throughout the collection, processing, analysis and interpretation steps?
* Why did you choose the research methodologies you used?

## The rationale to map the business requirements to the Data Visualisations
* List your business requirements and a rationale to map them to the Data Visualisations

## Analysis techniques used
* List the data analysis methods used and explain limitations or alternative approaches.
* How did you structure the data analysis techniques. Justify your response.
* Did the data limit you, and did you use an alternative approach to meet these challenges?
* How did you use generative AI tools to help with ideation, design thinking and code optimisation?

## Ethical considerations
* Were there any data privacy, bias or fairness issues with the data?
* How did you overcome any legal or societal issues?

## Dashboard Design
* There is only one interactive dashboard page in PowerBI. 
* It has a large heart image to represent what the main topic of the dashboard is, which is heart failure analysis. 
* To prove the age and gender as predictors hypothesis, created demographic bar charts to compare risk score for different age groups and genders. 
* Created a pie chart to highlight the number of patients at risk and what their respective risk level was based on high, medium, normal and low risk category.
* Created multiple option selection options for Risk level and Chest Pain Type to get relevant figures and analysis.
* 
![Dashboard Design]
* Later, during the project development, you may revisit your dashboard plan to update a given feature (for example, at the beginning of the project you were confident you would use a given plot to display an insight but subsequently you used another plot type).
* How were data insights communicated to technical and non-technical audiences?
* Explain how the dashboard was designed to communicate complex data insights to different audiences. 

## Unfixed Bugs
* There are no unfixed bugs.
* Did you recognise gaps in your knowledge, and how did you address them?
I would take a break, then troubleshoot with Copilot and ChatGPT AI about what I exactly wanted the code to do and produce and would try different commands to get the exact code and outlook I wanted. 

* If applicable, include evidence of feedback received (from peers or instructors) and how it improved your approach or understanding.

## Development Roadmap
* What challenges did you face, and what strategies were used to overcome these challenges?
I spent lot of time on creating plots and graphs in data visualisation jupyter notebook and struggled to recreate them in PowerBI, I even exported all the visuals created using plotly as html files with the intent to create a Tableau dashboard instead but dropped that idea as I already had a dashboard halfway done in PowerBI and tried to create the possibly relevant graphs for a non-technical person in a PowerBI dashboard.

Another time-consuming challenge I faced was that I spent more than two days creating different predictive models, finally selecting Logistics Regression Model (LRM) for its beter Recall result and wanted to predict risk score and risk level for the whole dataset and export it into two new columns in dataframe and export it into a new csv file but there was some variable mixup that only the trained dataset chunk was being exported. Fixed the code by meticulously going through the predictive modelling with Copilot AI to spot and fix the issue.  

* What new skills or tools do you plan to learn next based on your project experience? 
I would like to explore Streamlit and Heroku a bit more in the future to create independent dashboards. I will also conduct some experiments to create dashboards in Plotly Dash and Tableau for practice.


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

* Kaggle Dataset: https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction
* Inspired by https://www.kaggle.com/code/tanmay111999/heart-failure-prediction-cv-score-90-5-models/notebook

### Content & Media

-  Most of the code was developed with the assistance of Copilot and ChatGPT AIs

- The Code Institute logo is from (https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)
- The heart image was generate by using Copilot
- The dashboard wireframe was made in Balsamic Wireframes app
- Rest of the diagrams are exported from the project's Data Visualisations jupyter notebook


## Acknowledgements
* Thanks to Vasi and Niel and my incredibly talented peers in my cohort for providing support through this project.