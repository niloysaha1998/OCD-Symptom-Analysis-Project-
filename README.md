# OCD-Symptom-Analysis-Project-
Systematic exploratory analysis, logistic regression and rank tool have been utilised to investigate the effect of age on OCD symptom variation

## Title:
### "A Comprehensive Analysis of Age Related Variability in OCD Diagnosed Patients and OCD Diagnosis"



### Background

Obsessive-Compulsive Disorder (OCD) is characterized by persistent, unwanted thoughts (obsessions) and repetitive behaviors (compulsions), often involving actions like frequent washing, checking, or counting. Affecting at least 3% of the global population, it significantly impacts daily functioning, and early detection is critical to prevent it from becoming chronic. However, symptoms vary greatly, making personalized treatment challenging, and there is limited research exploring the relationship between age and symptom severity. This project aims to investigate the effect of age on the variation and severity of symptoms in OCD-diagnosed patients and explore whether OCD diagnosis is based on different symptoms across age groups. Upon completion, this research will help identify patterns in OCD symptoms according to age groups and provide insights into whether doctors use different evaluation metrics for symptom assessment across these groups.

### Dataset Description

The dataset is created from the survey responses to Symptom Checklist- 90 (SCL-90)
questionnaire which is a recognized tool to measure psychological problems. The responses are
collected from 5858 individuals including both OCD diagnosed and regular person. This dataset
was collected from the National Institute of Medicine. It has 5858 rows where each row represents
individual responses. The key variables for this research in this dataset are Age, Survey
responses (C_1 to C_90) and class. Class variable shows only binary numbers where 0 means
negative and 1 means positive referring to the existence of OCD in that person. A new variable
called ‘Age Group’ has been created to categorize the age data into Child (Child(1-12), Adolescent
(13-17), Young Adult (18-35), Adult (36-55), Senior(56-Rest).The child category does not have
many respondents, thus this category of data has been avoided for analysis and also the rows
where response to a variable is missing has been avoided.

### Analysis

#### Part 1: Effect of Age on the Already OCD Diagnosed Patients

![image](https://github.com/user-attachments/assets/7f417800-782d-4efc-af2e-0b35c590f337)



Comment: Most of the survey responses are from individuals belonging to the adult and young adult category.
But there are sizable number of responses from senior and adolescent population which is
important to proceed towards the aim of this project. The mean, median and standard deviation
in the dataset also provide important insight into which symptom are the most common among
the respondents irrespective of their OCD diagnosis.

![image](https://github.com/user-attachments/assets/5bd20c00-769f-4d5b-b058-66d7bd4b2936)

Comment: To understand and interpret better, the analysis has been segmented according to age group
and the percentage of respondents with OCD who select 3-5 scale (meaning strong symptom)
in each symptom question has been identified. From figure 2, it can be observed that 6 symptoms have more than 60% of responses in the 3-5
scale meaning that these symptoms are existent on moderate to high level in most OCD
diagnosed senior respondents. 

![image](https://github.com/user-attachments/assets/1da9c229-e4fc-49b7-a297-0f2fd912391d)

Comment: From figure 3, it can be interpreted that about 10 symptoms are commonly exhibited by the adult
population diagnosed with OCD.

![image](https://github.com/user-attachments/assets/e59eed1e-420c-4d5a-b9b1-fc261f744f3c)

Comment: From figure 4, it can be interpreted that about 10 symptoms are commonly severe among the
‘Young Adult’ population which are mentioned in the table above as well.

![image](https://github.com/user-attachments/assets/e188d3ad-4d88-41c0-92f9-888cb0c6d807)

Comment: From figure 5, it can be interpreted that about 10 symptoms are commonly severe among the
‘Young Adult’ population which are mentioned in the table.

![image](https://github.com/user-attachments/assets/98c9f87d-f0be-421b-a9f8-8d895b2978ee)

Comment: To understand if there is variance and severity of symptoms in the OCD diagnosed individuals,
the graph above provides a strong reference point as it combines the analysis in the age
segmented graphs and provides a uniform overview on whether the symptoms change with the
change in age in OCD diagnosed respondents.

![image](https://github.com/user-attachments/assets/143df8e2-1f13-4ee7-baa0-22de819271a8)


##### Insights

There are some common symptoms that are exhibited by any OCD
diagnosed patients including lonliness, unwanted thoughts, worrying too much etc. But there are unique symptoms as well, that are present only in a specific age group of
individuals. For example,  “feeling of getting easily
annoyed” is only expressed as a symptom by OCD patients from the senior age group. As we
have only selected the top 5 symptoms from each age group, there might be other unique
symptoms that are not presented in the graph. But as a generalisation, it can be stated that there
are symptoms which are unique to particular age group. So in terms of treatment intevention, there
needs to be personalisation according to the profile of OCD patient.


#### Part 2: Effect of Age on the Diagnosis of OCD in the Initial Screening

The following analysis will look to explore around diagnosis of OCD in individuals in the first place
and how the symptom criteria vary across different age group in diagnosing OCD in an individual.
We have conducted a rank analysis through the orange tool, where we have taken ‘Class’ as our
dependent variable and the symptom questions as independent variable. This means that the tool
will do a rank analysis on the symptom variables which have the most impact on the change of
‘Class’ variable.

![image](https://github.com/user-attachments/assets/c7ddd005-4d5e-4cc0-b53c-3fdaf7d52a01)

![image](https://github.com/user-attachments/assets/9345fbad-58a4-4f1c-811a-cc8f9de22598)


##### Insights

The analysis reveals that while there are common symptoms used as a basis for diagnosing OCD across all age groups, certain symptoms are unique to specific age groups. For instance, difficulty making decisions is a universal indicator for diagnosing OCD regardless of age, whereas unwanted thoughts are a key diagnostic criterion primarily for the young adult age group. This variability highlights that the importance placed on certain symptoms by doctors varies depending on the patient’s age group, emphasizing the need for age-specific evaluation metrics in diagnosing OCD.

#### Part 3: Model Validation

![image](https://github.com/user-attachments/assets/4371f69f-55c0-4278-99d6-fbdd169e254d)

Comment: We used the 10-fold cross validation model which splits the dataset into 10 equal parts adjusting
for overfitting and providing a reliable result. The performance metrics that were used include
AUC, accuracy, F1 score, precision, recall and mcc. Any metric with results above 70% can be
considered a sign of model reliability. All the evaluation criteria for all four models show results above 70% which is considered as
threefold for considering a model reliable for interpretation. So, the results from the rank tool can
be used as evidence for concluding the objective of this research.

### Results
The purpose of this project was to evaluate the OCD related dataset of 5858 respondents on 2
dimensions; one is to investigate whether OCD diagnosed individuals exhibit different symptoms
across age groups, second is to explore if even the symptom criteria of OCD diagnosis also varies
across age groups. The descriptive analysis that we have done strongly indicates that there are variations in
symptoms in the OCD positive patients across different age groups. The graphs presented us
with evidence that certain symptoms are unique to particular age group as far as OCD positive
patients are concerned. This is an important reference to the idea that OCD patients need
customized and personalized treatment as symptoms vary across different ages. The importance of personalization is further evidenced in our analysis of overall dataset where
we implemented regression and rank methods to identify the most influential symptoms in
diagnosing someone with OCD across age groups. This objective comes from the assumption
that the symptoms that are considered important in OCD determination also change with age
group. In summary, it means that the doctors who are diagnosing OCD are basing
the diagnosis on different symptoms considering the age group of the individual person.















