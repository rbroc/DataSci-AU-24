### Class 2 - Modeling problems

## Personality and random numbers
We will focus on predicting random number choices from personality scores.
**Outcome (Y)**, choose one of the following: 
    - `R18`, i.e., the last choice of a number between 1 and 100
    - Binned versions of `R18` (extremes - middle - other? round versus other?)
    - **Bonus**: predict multiple responses at once
**Models**:
    - Model 0 (dummy baseline): Always predict the _median_ (or _mode_?) of Y on the training data
    - Model 1a: Predict Y based on other answers to 1-100 questions
    - Model 1b: Predict Y based on other random number picks
    - Model 2: Include personality scores as predictors 

## Bike sharing
Let's focus on predicting the number of users based on weather and temporal information
**Outcome (Y)**, choose one:
- Total number of bikers `cnt`
- Count of casual or registered users (`casual` or `registered`)
- **Bonus**: the difference or ratio between registered and casual
**Models**
    - Model 0 (dummy baseline): Always predict the average of Y in the training data
    - Model 1: Predict based on a linear model with `instant` as the only predictor
    - Model 2: Model including weather info (temperature, windspeed) and temporal parameters (e.g., `season`, `weekday`) as predictors
    - Model 3: A "kitchen sink" model, will all predictors included
