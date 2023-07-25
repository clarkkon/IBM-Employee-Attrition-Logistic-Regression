# Logistic Regression and Employee Attrition (Phase 3 Project Submission)

## Overview and Business Understanding/Questions

My stakeholder is IBM, and the company wishes to mitigate employee attrition.  

They would like advice on what aspects of employment potentially contribute to employee attrition.

Business Questions:

What features increase an employee's likelihood to leave IBM the most?

What features reduce an employee's likelihood to leave IBM the most?

## Data Source and Exploration

This data comes from the IBM HR Analytics Employee Attrition & Performance dataset at the following site: https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset.  Click the link, then click download to download the dataset as a csv file, labeled WA_Fn-UseC_-HR-Employee-Attrition.csv.  For reproducibility, you will need either to rename the file employee_attrition.csv or replace df = pd.read_csv('employee_attrition.csv') in cell one of the notebook with the following: df = pd.read_csv('WA_Fn-UseC_-HR-Employee-Attrition.csv'). 

All features in the dataset were used. The most relevant were:
* Total Working Years
* Years in Current Role
* Job Level
* Number of Companies Worked
* Distance from Home


I created the following visualizations from this data (among many others, see notebook labeled index.ipynb for all visualizations):

![Correlation Between Attributes](https://github.com/clarkkon/IBM-Employee-Attrition-Logistic-Regression/assets/98120389/5a3ba293-74e1-48b9-86c8-889dca3eadc5)

![Attrition and Total Working Years](https://github.com/clarkkon/IBM-Employee-Attrition-Logistic-Regression/assets/98120389/990b1d76-f550-45eb-a987-3e5554ffd203)

![Attrition and Years in Current Role](https://github.com/clarkkon/IBM-Employee-Attrition-Logistic-Regression/assets/98120389/1486a931-7011-4ec2-a952-9f07804d76d7)

![Attrition and Job Level](https://github.com/clarkkon/IBM-Employee-Attrition-Logistic-Regression/assets/98120389/17ae2068-58b5-41f6-9fd3-da9f0eb0cf27)

I ran a basic Logistic Regression model, and then ran XGBoost to create an improved model. I attempted to boost that model with GridSearchCV, but that proved ineffective.

This resulted in a model with the following evaluation metrics:
Training Accuracy: 100.0%
Validation Accuracy: 86.96%
Training Precision: 100.0%
Validation Precision: 50.0%
Training Recall: 100.0%
Validation Recall: 33.33%
Training F1 Score: 100.0%
Validation F1 Score: 40.0%

Below is my Confusion Matrix for the model:

![Confusion Matrix](https://github.com/clarkkon/IBM-Employee-Attrition-Logistic-Regression/assets/98120389/5e176215-4101-4399-b22d-e3849c37cdce)

## Conclusion and Recommendation

IBM should consider the following when mitigating risks of employee attrition:

Employee attrition slightly increases as the number of companies worked and the distance from home increase. 

IBM should be cautious when hiring employees who have worked for a large number of companies, and incentivize those employees to stay if they wish to mitigate attrition.  Employees who live far from home could also be incentivised to move closer to their place of work, perhaps through relocation packages.  

Employee attrition decreases as total working years, number of years in current role, and job level increase. 

The longer an employee has been with IBM, and the higher job level they have obtained, the more likely that employee is to stay with the company. IBM should incentivize longevity with the company, perhaps through stock or other perk options, and should maintain pathways of upward mobility for employees. 

More information is needed to act on this information. IBM should conduct further surveys to investigate why more senior employees have stayed, and why more junior employees may leave. Consider more qualitative data to help unpack quantitative survey questions, and consider further inquiries regarding diversity and belonging to determine whether there is a pattern in the type of employee attrition that is taking place. 


## Navigating the repository:

Data for this project can be found in employee_attriion.csv file

Images for README can be found in the image folder.

index.ipynb contains the coding and markup

presentation.pdf is PowerPoint presentation of my information for my stakeholder, the link for which presentation can be found [here](https://docs.google.com/presentation/d/1cg4bz9WO3JMktPdvxqbhGGsCYClR589xYYdrvFqUKxY/edit?usp=sharing).
