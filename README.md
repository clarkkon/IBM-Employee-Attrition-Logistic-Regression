# Logistic Regression and Employee Attrition (Phase 3 Project Submission)

## Overview and Business Understanding/Questions

My stakeholder is IBM, and the company wishes to mitigate employee attrition.  

They would like advice on what aspects of employment potentially contribute to employee attrition.

What features increase an employee's likelihood to leave IBM the most?

What features reduce an employee's likelihood to leave IBM the most?

## Data Source and Exploration

This data comes from the IBM HR Analytics Employee Attrition & Performance dataset at kaggle.com.

All features in the dataset were used. The most relevant were:
* Total Working Years
* Years in Current Role
* Job Level
* Number of Companies Worked
* Distance from Home


I created the following visualizations from this data:
![Heat Map of Correlating Features](https://user-images.githubusercontent.com/98120389/217927030-e00c3912-a63b-4d16-86ad-143e2eeaf84e.png)

![Attrition and Total Working Years](https://user-images.githubusercontent.com/98120389/217927152-0c8d4c86-6d17-4383-b13c-2c320ef25cfc.png)

![Attrition and Years in Current Role](https://user-images.githubusercontent.com/98120389/217927172-d1aeb9a1-2554-412e-8a1a-af0ec64ed300.png)

![Attrition and Job Level](https://user-images.githubusercontent.com/98120389/217927186-b399322c-692b-48ac-903d-dd77832d64fb.png)


I ran XGBoost to create an improved model, and utilized GridSearchCV to improve upon that model. 

This resulted in a model with a Training Accuracy of 93.92% and a Validation Accuracy of 88.32%.

Below is my Confusion Matrix for the model:

![Attrition Model Confusion Matrix](https://user-images.githubusercontent.com/98120389/217927922-a4e54c7a-3785-4f93-b47f-cca8da4832cb.png)


## Conclusion and Recommendation

IBM should consider the following when mitigating risks of employee attrition:

Employee attrition slightly increases as the number of companies worked and the distance from home increase. 

IBM should be cautious when hiring employees who have worked for a large number of companies, and incentivize those employees to stay if they wish to mitigate attrition.  Employees who live far from home could also be incentivised to move closer to their place of work, perhaps through relocation packages.  

Employee attrition decreases as total working years, number of years in current role, and job level increase. 

The longer an employee has been with IBM, and the higher job level they have obtained, the more likely that employee is to stay with the company. IBM should incentivize longevity with the company, perhaps through stock or other perk options, and should maintain pathways of upward mobility for employees. 

More information is needed to act on this information. IBM should conduct further surveys to investigate why more senior employees have stayed, and why more junior employees may leave. Consider more qualitative data to help unpack quantitative survey questions, and consider further inquiries regarding diversity and belonging to determine whether there is a pattern in the type of employee attrition that is taking place. 
