# AI Data Linear Regression
In this project, I used Linear Regression to analyze and predict salaries for AI and Data Science roles. Using a synthetic Kaggle dataset of 5,000 AI/Data Science jobs, the project predicts how factors such as experience level, company location, education, and other variables correlate with salary. 

The analysis also evaluates the limitations of standard linear regression models and tests if transforming the target variable can improve prediction performance. 

## Project Objective 
The First Objective of this project was to predict `salary_usd` and determine what features had the strongest or weakest association with compensation in the field of AI and Data Science.

The second objective is to evaluate the model through residual analysis and determine if a log transformation of salary can improve the accuracy and address the weakness of the original model. 

## Results 
The baseline Linear Regression model achieved 
- **R²:** 0.779
- **MAE:*** $19,588
- **RMSE:** $26,134

 The residual analysis showed that prediction errors became larger at the higher-end salaries, and my original scatterpoint model had produced some unrealistic negative salary predictions.
 This led me to train a second model using `log(salary_usd)`, which improved performance:
 - **R²:** 0.831
- **MAE:*** $15,837
- **RMSE:** $22,808

By using a log transformation, it improved the model in all three evaluation metrics and erased the problem of negative salary predictions

After finishing this project, we took a final bar graph of the 'Impact of Each Factor on Salary.' we observed from the model that factors like seniority, company location, education level, and "ML" in the job title had the strongest impacts on salary

## Technologies Used
- Python
- Pandas
- NumPy
- Malplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook 
