
# Introduction

In this project, machine learning modelling such as classification models, data understanding and data preparation, visualization and model evaluation was used to find the probabilty of the H1N1 Vaccine and seasonal flu vaccine.

# Project Overview
## Overview
## Business Problem
In the awaking of 2020, COVID-19 became a huge dilemma that took the world by storm. Millions ended up dying from the virus. Governments across the globe have started and have already distributed the COVID-19 vaccines.

This project will revisit the public health response to a different recent major respiratory disease pandemic and try predict the probability of people taking the COVID-19 vaccine.

In early 2009, Swine Flu (H1N1 virus) became a pandemic and it swept the world and around 150,000 - 500,000 deaths were recorded globally.

In October 2009, a vaccine against the H1N1 flu virus became widely available. The National 2009 H1N1 Flu Survey was conducted in the United States in late 2009 and early 2010. This phone survey asked respondents if they had received the H1N1 and seasonal flu vaccines, as well as personal questions. These additional questions focused on their social, economic, and demographic backgrounds, perspectives on illness risks and vaccine effectiveness, and behaviors aimed at preventing transmission. A better understanding of how these traits are related to personal vaccination patterns can help guide future public health efforts. 
## Aim of the project
The health sector has had a lot of pressure in dealing with the pandemics and also the governments have struggled with the distribution of the vaccined created by the scientists. The Aim of the project is to find the probabilities of people to get vaccinated with the COVID-19 vaccine through the analysis of the Swine Flu vaccination data. 
## Questions to answer
    The studio with the most movies
    What genres are most produced
    The language of the movie that is most popular
    How the year of production has affected it worldwide_gross

# 3. Data Understanding

The data used in this project was gotten from a competition in <a href = 'https://www.drivendata.org/competitions/66/flu-shot-learning/page/211/'> Driven Data</a> website.

## 3.1 Labels
There are two target variables for this competition:
<br><br>
<div class="alert alert-block alert-success">

**Observation:**<br>

h1n1 vaccine - Indicates whether the respondent received an H1N1 flu vaccine.<br><br>

seasonal vaccine - Indicates whether the respondent received the seasonal flu vaccine.<br><br>

Both are binary variables, with 0 indicating no and 1 indicating yes.<br>
Some respondents did not receive either vaccine, while others received only one or both.<br>
This is written as a multilabel (rather than a multiclass) problem. <br>
    </div>

## 3.2 Features

You've been given a dataset with 36 columns.<br>
Respondent id is a unique and random identifier in the first column.<br>
The remaining 35 features are discussed further below.<br>

<div class="alert alert-block alert-success">


For all binary variables, **0 equals No and 1 equals Yes.**<br><br>

* h1n1_concern - Level of concern about the H1N1 flu.<br>

_0 = Not at all concerned; 1 = Not very concerned; 2 = Somewhat concerned; 3 = Very concerned._<br><br>

* h1n1_knowledge - Level of knowledge about H1N1 flu.<br>

_0 = No knowledge; 1 = A little knowledge; 2 = A lot of knowledge._<br><br>

* behavioral_antiviral_meds - Has taken antiviral medications. (binary)<br><br>
* behavioral_avoidance - Has avoided close contact with others with flu-like symptoms. (binary))<br><br>
* behavioral_face_mask - Has bought a face mask. (binary))<br><br>
* behavioral_wash_hands - Has frequently washed hands or used hand sanitizer. (binary))<br><br>
* behavioral_large_gatherings - Has reduced time at large gatherings. (binary))<br><br>
* behavioral_outside_home - Has reduced contact with people outside of own household. (binary))<br><br>
* behavioral_touch_face - Has avoided touching eyes, nose, or mouth. (binary))<br><br>
* doctor_recc_h1n1 - H1N1 flu vaccine was recommended by doctor. (binary))<br><br>
* doctor_recc_seasonal - Seasonal flu vaccine was recommended by doctor. (binary))<br><br>
* chronic_med_condition - Has any of the following chronic medical conditions: asthma or an other lung condition, diabetes, a heart condition, a kidney condition, sickle cell anemia or other anemia, a neurological or neuromuscular condition, a liver condition, or a weakened immune system caused by a chronic illness or by medicines taken for a chronic illness. (binary)
* child_under_6_months - Has regular close contact with a child under the age of six months. (binary)
* health_worker - Is a healthcare worker. (binary)<br><br>
* health_insurance - Has health insurance. (binary)<br><br>
* opinion_h1n1_vacc_effective - Respondent's opinion about H1N1 vaccine effectiveness.<br><br>
_1 = Not at all effective; 2 = Not very effective; 3 = Don't know; 4 = Somewhat effective; 5 = Very effective._<br><br>
* opinion_h1n1_risk - Respondent's opinion about risk of getting sick with H1N1 flu without vaccine.<br>
_1 = Very Low; 2 = Somewhat low; 3 = Don't know; 4 = Somewhat high; 5 = Very high._<br><br>

* opinion_h1n1_sick_from_vacc - Respondent's worry of getting sick from taking H1N1 vaccine.<br>
_1 = Not at all worried; 2 = Not very worried; 3 = Don't know; 4 = Somewhat worried; 5 = Very worried._<br><br>
* opinion_seas_vacc_effective - Respondent's opinion about seasonal flu vaccine effectiveness.<br>
_1 = Not at all effective; 2 = Not very effective; 3 = Don't know; 4 = Somewhat effective; 5 = Very effective._<br><br>
* opinion_seas_risk - Respondent's opinion about risk of getting sick with seasonal flu without vaccine.<br>
_1 = Very Low; 2 = Somewhat low; 3 = Don't know; 4 = Somewhat high; 5 = Very high._._<br><br>
* opinion_seas_sick_from_vacc - Respondent's worry of getting sick from taking seasonal flu vaccine.<br>
_1 = Not at all worried; 2 = Not very worried; 3 = Don't know; 4 = Somewhat worried; 5 = Very worried._._<br><br>
* age_group - Age group of respondent.
* education - Self-reported education level.
* race - Race of respondent.
* sex - Sex of respondent.
* income_poverty - Household annual income of respondent with respect to 2008 Census poverty thresholds.
* marital_status - Marital status of respondent.
* rent_or_own - Housing situation of respondent.
* employment_status - Employment status of respondent.
* hhs_geo_region - Respondent's residence using a 10-region geographic classification defined by the U.S. Dept. of Health and Human Services. Values are represented as short random character strings.
* census_msa - Respondent's residence within metropolitan statistical areas (MSA) as defined by the U.S. Census.
* household_adults - Number of other adults in household, top-coded to 3.
* household_children - Number of children in household, top-coded to 3.
* employment_industry - Type of industry respondent is employed in. Values are represented as short random character strings.
* employment_occupation - Type of occupation of respondent. Values are represented as short random character strings.
    </div>
Data cleaning was done by dropping missing values and filling the usable missing values. Also done was the merging of tables to have more data to use while analyzing.

# Exploratory Data Analysis (EDA)


## Screenshots
### 1. Does sex has affected the distribution of the vaccine?
#### img 1.
![App Screenshot](IMG1.png)
![App Screenshot](IMG2.png)
### 2. Does race affect the distribution of the vaccine?
#### img 1.
![App Screenshot](IMG3.png)
![App Screenshot](IMG4.png)
#### img 2.
![App Screenshot](IMG5.png)
![App Screenshot](IMG6.png)
#### img 3.
![App Screenshot](IMG7.png)
![App Screenshot](IMG8.png)
### 3. Does Education level affect the distribution of the vaccine?
#### img 1.
![App Screenshot](IMG9.png)
![App Screenshot](IMG10.png)
### 4. Does Location affect the distribution of the vaccine?
#### img 1.
![App Screenshot](IMG11.png)
![App Screenshot](IMG12.png)
### 5. Does homeownership affect the distribution of the vaccine?

![App Screenshot](IMG13.png)
### 6. How the chronic illnesses has affected the distribution of the vaccine?
#### img 1.
![App Screenshot](IMG14.png)
![App Screenshot](IMG15.png)

### 7. Does Age group affect the distribution of the vaccine?
#### img 1.
![App Screenshot](IMG16.png)
![App Screenshot](IMG17.png)

## Modelling

![App Screenshot](IMG18.png)

## Conclusion
Incorporate more variables: The model could benefit from incorporating more variables that could affect vaccine uptake, such as demographic factors (e.g., age, income, education), personal beliefs (e.g., perception of vaccine safety, efficacy), and access to healthcare. Utilize recent data: The model's training data should be updated to include the most recent information to reflect changes in vaccine uptake patterns. Tune the model: The model can be further improved by fine-tuning its
Tune the model: The model can be further improved by fine-tuning its parameters to increase its accuracy. This can be done through techniques such as cross-validation, which involves splitting the data into training and validation sets, and using the validation set to evaluate the model's performance. Consider alternative models: It may also be worth exploring alternative machine learning models, such as decision trees or random forests, to see if they perform better in predicting vaccine uptake. Conduct additional research: Finally, it would be useful to conduct additional research to identify new factors that could impact vaccine uptake and incorporate them into the model. This could involve surveys, focus groups, or other forms of qualitative research to gain a deeper understanding of people's attitudes and behaviors towards vaccines.



## Recommendation
* Through the model predictions we can recommend the governments to do more public education on the importance of the vaccines and mostly focus on the 34-44 years age group.
● The vaccines should be made more available and accessible to all people and most importantly those with chronic illnesses.
