# DSCI 100 Project

## Research Question
Question 1: What player characteristics and behaviours are most predictive of subscribing to a game-related newsletter, and how do these features differ between various player types?

## Dataset
- Name: players.csv
- Source: UBC Computer Science Research Minecraft Server (Frank Wood Lab)
  
## Dataset Usage
Although both `players.csv` and `sessions.csv` were originally loaded, only `players.csv` was used in final analysis. 
My research question focuses on how player characteristics relate to whether a player subscribes to the research newsletter. 
The variables I focused on were experience level, played_hours, age, and gender, and all of these are already included in `players.csv`. 
Because of that, I didn’t need to use `sessions.csv` for this project.

## Variables Used
- `hashedEmail`: Unique anonymized ID for each player
- `Age`: Player age in years
- `gender`: Self-reported gender identity
- `experience`: Self-reported Minecraft experience level (e.g., Beginner, Amateur, Pro)
- `played_hours`: Total number of hours the player has played
- `subscribe`: Whether the player subscribed to the newsletter (TRUE/FALSE)

## Model Selection Plan

Since my research question involves predicting whether a player subscribed to the newsletter (a Yes/No outcome), I plan to use a K-Nearest Neighbors (KNN) classification model.

KNN is appropriate because it works well for categorical outcomes and does not make strong assumptions about the data. Before applying the model, I will standardize the numeric variables so that distance calculations are fair. I will also convert categorical variables into factors.

To choose an appropriate value of *k*, I will test several values and compare their performance using cross-validation. I will evaluate the models based on accuracy and the confusion matrix results to see how well the model distinguishes subscribers from non-subscribers.

After evaluating the results, I will select the value of *k* that provides the best classification performance and use that version of the model for the final prediction and interpretation.
