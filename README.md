# Predicting AI & Data Science Salaries with Linear Regression

In this project, I used linear regression to analyze and predict salaries for AI and Data Science roles. Using a synthetic Kaggle dataset of 5,000 AI/Data Science jobs, the project examines how factors such as experience level, company location, education, and other variables are associated with salary.

The analysis also evaluates the limitations of a standard linear regression model and tests whether applying a log transformation to the target variable can improve prediction performance.

## Project Objective

The first objective of this project was to predict `salary_usd` and determine which features had the strongest or weakest associations with compensation in the fields of AI and Data Science.

The second objective was to evaluate the model through residual analysis and determine whether a log transformation of salary could improve accuracy and address weaknesses in the original model.

## Results

| Model | R² | MAE | RMSE |
|---|---:|---:|---:|
| Original Linear Regression | 0.779 | $19,588 | $26,134 |
| Log-Transformed Linear Regression | **0.831** | **15,837** | **22,808** |

The actual vs. predicted salary scatter plot showed that prediction errors became larger at higher salary levels, and the original model also produced some unrealistic negative salary predictions. Residual analysis further confirmed that the model's errors were not evenly distributed.

This led me to train a second model using `log(salary_usd)`, which improved performance:

The log transformation improved the model across all three evaluation metrics and eliminated the problem of negative salary predictions.

Finally, I created a bar graph showing the impact of each factor on salary. The model showed that factors such as seniority, company location, education level, and having "ML" in the job title had some of the strongest associations with salary.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Limitations

- This dataset is synthetic, so the results may not fully represent real-world salary patterns.
- Linear regression may not capture complex relationships between job characteristics and salary.
- The relationships found by the model show associations, not proof that specific factors directly cause changes in salary.

## Author

**Noah Alexander Weir-Shack**  
Data Science Major, University of Pittsburgh
