# Car auction Practice
Scenario: We are provided with a car auction dataset. Our goal is to (1) Build prediction model using Random Forest, and (2) Explain 
the effects of the most important features on predictions (using global and local analysis) with following procedures:

1. Import the dataset. Current version includes no missing values.
2. Examine the distribution of the outcome variable winning_or_high_bid and decide if we need to transform 
it or not. Proceed with either original or transformed outcome based on our decision. 
3. Establish a baseline Random Forest model using:
- all appropriate (scaled) features,
- default parameters,
- random_state = 0 (remember to include it twice), and 
- test_size=0.2,
4. Use GridSearchCV to try different parameters and associated values to improve we baseline model. Rely 
on our knowledge and documentation to select appropriate parametrization.
5. Run our Random Forest model with “best” parameters. Were we able to improve accuracy?
6. Check the coefficient of determination of our “best” performing model and provide a brief conclusion. 
7. Using SHAP library, generate shap_values for our “best” performing model on the training set. 
8. Create a summary plot and describe our observations:
- What are the top 5 most influential predictors? 
- What is the direction of the effects for the top 5 most influential predictors?
- There is a pair of variables in the top 5 which are likely to be strongly correlated – what is this pair? To 
answer this question, we need to recall what each feature actually means OR examine their correlations. 
9. Using SHAP library, generate shap_values for our “best” performing model on the validation set. 
10. Create a force plot and describe the results for the 5th observation in our validation set:
- Which factor(s) increase prediction?
- Which factor(s) decrease prediction?
11. Find out the ID of the 5th observation and provide practical recommendations to improve listing 
performance based on observed values of the factors that increase/decrease price prediction. 
