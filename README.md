# Phase 3 Project 
## BY MONICA MWANGI

# FORECAST INDIVIDUALS' H1N1 AND SEASONAL FLU VACCINE UPTAKE

![image](https://github.com/PennyGituku/dsc-phase-3-project-v2-3/assets/133040605/e179987b-b3aa-4b98-8c63-4558c623f724)



# TABLE OF CONTENTS

* Business Understanding

* Problem Statement

* Proposed Solution

* Specific Objectives

* Research Questions

* Success Criteria

* Data Analysis

* Conclusion
  

# Business Understanding
  ## Project Overview

![Vaccine](https://media.tenor.com/3nkEeVR-IOYAAAAC/needle-injection.gif)

Seasonal influenza or the Flu is an acute respiratory infection caused by influenza viruses all over the world and most people tend to recover without treatment. [Symptoms include acute onset fever, cough, sore throat, body aches, and fatigue.](https://www.who.int/news-room/fact-sheets/detail/influenza-(seasonal))

[The H1N1 flu, sometimes called Swine flu is a type of influenza A virus. During the 2009-10 flu season, a new H1N1 virus began causing illness in humans and it was often called Swine flu and was a combination of influenza viruses that infect pigs, birds, and humans. The World Health Organization (WHO) declared the H1N1 flu to be a pandemic in 2009. That year the virus caused an estimated 284,400 deaths worldwide. In August 2010, WHO declared the pandemic over. However, the H1N1 flu strain from the pandemic became one of the strains that cause seasonal flu. Most people with the flu get better on their own. But flu and its complications can be deadly, especially for people at high risk. The seasonal flu vaccine can now help protect against the H1N1 flu and other seasonal flu viruses.](https://www.mayoclinic.org/diseases-conditions/swine-flu/symptoms-causes/syc-20378103#:~:text=The%20World%20Health%20Organization%20(WHO,strains%20that%20cause%20seasonal%20flu.) 

[Influenza (flu) vaccines (often called “flu shots”) are vaccines that protect against the four influenza viruses that research indicates will be most common during the upcoming season. Most flu vaccines are “flu shots” given with a needle, usually in the arm, but there also is a nasal spray flu vaccine.](https://www.cdc.gov/flu/prevent/flushot.htm#:~:text=Influenza%20(flu)%20vaccines%20(often,a%20nasal%20spray%20flu%20vaccine.)

The CDC recommends flu vaccination for everyone aged 6 months and older in the United States since the 2010-2011 flu season. It is crucial for preventing flu and its complications, especially for those at higher risk. Suitability for vaccination or a specific vaccine depends on factors like age, health, and allergies. Various vaccines are approved for different age groups, and some are not recommended for specific individuals. Notably, there are three flu vaccines preferentially recommended for people aged 65 and older.

# Problem Statement

![gif](https://i.gifer.com/origin/f7/f748a43312487000f282968b97aa60fe.gif)

Faced with the reality of how quickly viral diseases like H1N1 and seasonal flu can spread, along with their associated health risks and a notable mortality rate, there is a pressing need to develop a model to accurately identify individuals who are more likely to receive their H1N1 and seasonal flu vaccines.

[During the H1N1 pandemic in 2009, the virus caused more than 284,000 deaths worldwide, according to the US Centers for Disease Control and Prevention. At that time, the World Health Organization declared H1N1 a pandemic virus. However, the virus is now circulating like a seasonal influenza virus.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3928226/#:~:text=In%20Canada%2C%20seasonal%20flu%20normally,for%20Disease%20Control%20and%20Prevention.)

Efficient identification of such individuals is not only essential to boost vaccination rates but also to significantly reduce the spread of influenza. This model can inform targeted interventions, resource allocation, and tailored information campaigns to ensure that those at higher risk of complications or those in frequent contact with vulnerable populations receive the necessary vaccinations.

The urgency of this task is underlined by the aim to leverage data-driven insights to enhance public health outcomes and to prevent the rapid transmission of these influenza strains, ultimately reducing mortality rates associated with these viral infections.
  
# Proposed Solution

- Develop data-driven predictive models for identifying individuals likely to receive H1N1 and seasonal flu vaccines.
- Utilize essential features, such as demographics and vaccination history, for accurate predictions.
- Collect and integrate data from diverse sources, including healthcare providers and public health agencies.
- Tailor information campaigns with personalized messaging to address vaccination concerns.
- Allocate resources strategically based on predictive model insights to improve vaccine accessibility.
- Implement real-time monitoring to adapt strategies to changing trends.
- Foster collaborative partnerships with healthcare providers and community organizations.
- Establish an evaluation and feedback loop to continuously enhance the accuracy of predictions and vaccination rates.

# Specific Objectives

Create a model to assess feature importance within the dataset, helping identify key factors to emphasize when promoting vaccination.

# Research Questions
  > Which model best predicts the likelihood of the H1N1 vaccine being taken?
  
  > Which key factors should be emphasized on when promoting vaccination?

# Success Criteria

> The Logistic Regression model demonstrates a good overall performance in predicting vaccine uptake.

> It has a high accuracy, suggesting that it makes correct predictions in most cases.

> However, to make it more effective, it might need improvements in precision and recall, especially in capturing all individuals who should take the vaccine (recall) while minimizing unnecessary vaccinations (precision).

> The model's performance can be done better with access to more features such as location and employment features that were encoded due to data privacy, the model has a high success rate and should be considered for deployment.

# Data Analysis
![image](https://github.com/PennyGituku/dsc-phase-3-project-v2-3/assets/133040605/cfab1e09-c9de-41d7-9c45-ea47eaeabfee)

The variables don't have a high correlation, seeing that the highest correlation is 0.58, thus there is no multicollinearity.

classification models used were:
> Logistic Regression: It's a simple and widely used model for binary classification. It's also extendable to multiclass classification.

The model achieved an accuracy of 85%, indicating it correctly predicted 85% of instances. However, it's less effective in identifying instances where the vaccine was taken (class 1), as shown by the lower recall and F1-score for class 1. The report helps assess the model's performance in predicting vaccine decisions.

![image](https://github.com/PennyGituku/dsc-phase-3-project-v2-3/assets/133040605/39ead0d1-9259-42ca-9733-237f6d9f8ea3)


The most important feature, 'opinion_h1n1_risk,' suggests that people's perception of the risk associated with the H1N1 virus plays a significant role in their decision to get vaccinated.
The 'seasonal_vaccine' feature is the second most important, indicating that whether individuals have received the seasonal flu vaccine in the past influences their decision to get the H1N1 vaccine.
'opinion_seas_risk' follows closely, indicating that people's perception of the risk associated with the seasonal flu is also an important factor.
'doctor_recc_h1n1' suggests that recommendations from doctors for the H1N1 vaccine are influential.
'opinion_seas_sick_from_vacc' and 'opinion_seas_vacc_effective' reflect individuals' opinions on the effectiveness and side effects of the seasonal flu vaccine.
Socioeconomic factors, such as income, poverty status, and employment status, play significant roles.
Demographic factors, including marital status, race, rent or own status, and sex, have varying levels of importance.
The number of adults and children in the household also influences vaccination decisions.
Being a health worker is among the least important factors.


> Decision Trees: These models are easy to understand and interpret. They can be used for both binary and multiclass classification.

The DecisionTreeClassifier performs reasonably well in identifying cases of vaccine uptake and no vaccine uptake, with balanced precision and recall for both classes. However, its overall accuracy is lower compared to the Logistic Regression model. It correctly identifies vaccine uptake about 51% of the time, suggesting potential for improvement or addressing class imbalances in the dataset.


> K-Nearest Neighbors (K-NN): It classifies data points based on the majority class among their k-nearest neighbors.

KNN performs moderately well but has lower recall and F1-score for identifying cases of vaccine uptake compared to Logistic Regression and Decision Tree. It seems to struggle with correctly identifying vaccine uptake cases, resulting in a lower overall accuracy. 

The logistic Regression classifier model was tuned and a  pipeline was created and saved in Joblib

# Conclusion

The logistic regression model displays promise in predicting vaccine uptake with considerations for improving precision and recall while socioeconomic and demographic factors play significant roles.
