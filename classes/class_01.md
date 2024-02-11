### Class 1 - Formulating predictive modeling questions

In the first class, we worked on exploring a dataset and formulating a predictive modeling question to work on.
Here is a log of the predictive modeling questions for each group.

## Personality and random numbers 
### Group 1
**Question 1**: Predict the answer to R18, i.e., choice of a number between 1 and 100. This question is repeated multiple times, and this is the last time it is asked.
Models:
- Model 0: Always predict the median of Y the training data
- Model 1: Predict Y based on other answers to 1-100
- Model 2: Include other random number picks
- Model 3: Include personality
- (opt) Model 4: Do feature engineering to construct columns encoding information on order of presentation and anchoring or consistency

**Question 2**: Predict personality from random numbers, either single-item (e.g., C7, "I like order") or for all questions (or predict aggregate scores)

### Group 2
**Question**: can scores on personality tests predict the quantile from which a number is chosen? The target variable is a binned version of the response, coding for lower, middle or upper quantile of the scaled response variable.
All scores from the personality questions are used for prediction.

- Model 0 (no-predictor baseline): using the most frequent bin as a predictor (your problem is not a regression problem, hence the mean does not make a lot of sense)
- Model 1 (single-predictor): using only one personality response
- Model 2 (several predictors): Using the scores of all five character traits as predictors

_To be addressed_
- Do you want to predict one of multiple targets simultaneously? I would suggest that, for these first steps, you select one target
- How do you define the boundaries of the bins? 
- It is fine as is, but why do you want to predict ranges, instead of either raw scores or things like: round versus non-round numbers; extremes, center or other?
- What is the rationale behind choosing one response to personality items as single predictor for a baseline? Do you want to consider choosing some other repsonse item as a predictor? Or just use models 
_A note_: You might want to take a look at quantile regression as an alternative to classification.


## Bike sharing
### Group 1
**Question 1**: How many bikes, (in total?), will be needed for a given season?
- Issue: Your training data will only be very few data points (one per season)?
**Question 2**: How does time of day and season affect bike rental?
- While this is not in principle a "wrong" question, it is mainly an inference question. Let's focus on its _predictive_ version: **can we predict the number of bikes that will be rented at a given time based on the season and the time of the day**?
**Questions 3**: Is there a difference in bike rental patterns between casual and registered users?
- Similar to Questions 2, this can be understood as an explanation / statistical testing question. To tackle this in statistical terms you could model the ratio or difference between registered and casual users as a function of your predictors?

### Group 2
**Question 1**: Can we predict the count of bikers (cnt) from weather predictors such as temperature (temp, could also be weathersit) and/or hour (hr) of the day?
**Question 2**: Can we predict the count of casual users (causal) from predictors such as week day, working day and temp? 

### Notes
**We have not specified a baseline yet, here are a couple of suggestions**:
- Model 0: Predict the average number of rentals in the training set (constant)
- Model 1: A linear model with `instant` as predictor (accounting for growth)
- Model 2: A model including weather and windspeed as predictors
- Model 3: A model including information on weekday and hour of the day as predictors
- Model 4: A "kitchen sink" model, with all relevant predictors