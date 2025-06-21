# Event Attendance Prediction using Semi-Supervised Learning

## Project Overview:
This project is focused on predicting whether people will attend a local event using a dataset collected from a Google Form. Since not all responses contain the actual attendance (Yes/No), we followed a semi-supervised learning approach to handle the incomplete labels.

## Objective:
The idea is to use the available labeled data to train a model and then use it to predict the missing labels. This helps us make use of all the responses instead of ignoring those without answers.

## Data Collection:
We created a Google Form and shared it with our classmates. The form had the following questions:
- Are you interested in the event topic?
- How far is the event from your place?
- Have you attended similar events before?
- Do you usually have free time during the event?
- Will you attend this event? (optional – only a few gave this)

We received more than 40 responses. The data was downloaded as a CSV file.

## ML Technique Used:
We used a method called **Self-Training** where:
1. We trained a basic model on the labeled data (where YES/NO was available).
2. Then, we predicted the missing values using that model.
3. After getting the predicted labels, we retrained the model with the full dataset.

We used a **Random Forest Classifier** as our main algorithm because it gave better accuracy and works well with small datasets.

## Prediction Sample:
After training, we tested the model by giving sample inputs.  
For example, when a person:
- is interested in the event
- lives 1-5km away
- has attended similar events before
- is usually free during the event time

The model predicted: **WILL ATTEND**

## Files Included:
- problem_statement.txt
- form_link.txt
- dataset.csv
- ml_code.ipynb (our model and preprocessing)
- model.pkl (saved model)
- output_screenshot.png (sample prediction)
- README.txt (this file)

## Team Info:
Team Name: HACK_TEAM3_PPS_KCET  
College: Kamaraj College of Engineering and Technology  
Date: 21-06-2025

