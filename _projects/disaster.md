---
layout: page
title: ML Disaster Relief
description: Leveraging ML for Disaster Risk Prediction and Resource Allocation 
img: /assets/img/ml/ml_cover.png
importance: 2
category: School
---

## Project Overview

This project focused on using **machine learning** to predict disaster severity and inform **resource allocation** strategies.  
We leveraged historical data from the [EM-DAT database](https://www.emdat.be/) to uncover patterns in global disasters by type, region, and severity — aiming to support data-driven humanitarian response efforts.

Completed as the final project for [CSCI 4622 – Machine Learning](https://experts.colorado.edu/display/coursename_CSCI-4622), this was a collaborative effort with **Stefan Bobick**, **Michael Sexton**, and myself — proudly known as *Team Disaster*.

Motivated by the pressing need for efficient disaster relief, the project aimed to showcase the practical application of machine learning techniques learned in class. The team's shared goal of advancing their understanding of ML models drove a commitment to finding actionable solutions for real-world problems.
<br><br>

---

## Data Preprocessing

We worked with a rich dataset consisting of **47 features and 26,378 disaster entries** dating back to 1900.  

Before modeling, we performed extensive **exploratory data analysis (EDA)** and data cleaning to uncover impactful patterns, define training features, and establish a target for classification.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="/assets/img/ml/ml_dis_freq.png" title="disaster_frequency" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="/assets/img/ml/ml_dis_deaths.png" title="deaths and type" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/ml/ml_type_region.png" title="type and region graph" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    These are some of the resulting plots from our EDA that helped us narrow down our focus and identify target variables to gauge different levels of impact and their relationship to certain types of natural disasters.  
</div>
<br><br>

---

## Machine Learning Models

The group utilized several machine learning approaches to address the challenges of predicting disaster risk, and optimizing resource allocation. Key models included:

#### `Random Forests Classifier (RFC)` 
* Implemented to classify disaster types based on key features such as the total number of people affected, region, country, date and duration of disaster. 

* Data preprocessing included encoding categorical variables using one-hot encoding, hyperparameter tuning via `RandomizedSearchCV` with 5-fold cross-validation optimized key parameters, and a feature importance analysis to rank features based on their influence on disaster type classification.

    - The model achieved an **accuracy** on the test set of `0.5699`. 
    - The top features influencing the classification and their respective importance:
        1. Total Affected: `0.248865`.
        2. Total Deaths: `0.229223`.
        3. Start Month: `0.154075`.
        4. Disaster Duration: `0.138568`.
<br><br>

#### `The Gradient Boosting Classifier (GBC)`
* Implemented to predict disaster severity using historical data features such as disaster type, location, time, and event duration. 
* Predicted **disaster severity** (Very Low to Very High) using log-transformed and normalized data.
* Similar to the `RFC` model, hyperparameter tuning was performed using `RandomizedSearchCV`, and a feature importance analysis was conducted.
    - The model achieved an **accuracy** on the test set of `0.5855`. 
    - The three best F1-Score for the predicted labels were:
        1. Very Low with a score of: `0.67`. 
        2. Moderate with a score of: `0.60`.
        3. Low with a score of: `0.52`. 
<br><br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ml/ml_pred_true_gbc.png" title="ml_pred_true_gbc" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ml/ml_gbc_cmatrix.png" title="ml_gbc_cmatrix" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    On the left, the count plot for the prediucted values from the classifier vs the true values from the dataset. On the right, the confusion matrix for the GBC classifier. 
</div>
<br><br>

---
## Technical Stack

- **Languages:** Python  
- **Libraries:** NumPy, Pandas, Scikit-learn, Matplotlib, Seaborn  
- **Techniques:** EDA, Feature Engineering, One-Hot Encoding, Hyperparameter Tuning  
- **Models:** Random Forest, Gradient Boosting  
- **Tools:** Jupyter Notebook, Git, VS Code
<br><br>

---

#### Conclusion 
Although our models fell short of initial expectations, they highlight both the potential and challenges of using machine learning for disaster classification and severity prediction. They offer valuable insights into disaster drivers that could enhance response and resource allocation. 

These results emphasize the need to combine advanced ML techniques with traditional disaster management for a more data-driven approach. 

Improving accuracy through better data, feature engineering, and exploring alternative models is a key next step.
<br><br>

---
## Project Poster

<div class="project-pdf mt-4">
    <iframe src="/assets/pdf/team_disaster_poster.pdf" width="100%" height="800px"></iframe>
</div>
