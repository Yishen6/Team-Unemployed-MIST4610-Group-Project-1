# Team Unemployed MIST4610 Group Project 1

## Team Name: 
15058 Unemployed

## Team Members: 

1. Ben Lim [gituser](link)
2. Jason Roode
3. Jack Schaeffer
4. Yirong Shen
5. Nathan To

## Problem Description: 

In order to provide the most efficient and organized method of patient intakes, we created a database showing the relationships between the various entities in a hospital environment. From taking in an appointment to seeing the actual patient, we strive to display how the hospital operates beyond what the patient experiences. To do this, we plan on using datamodels to show how the hospital staff work together, how billing and insurance relates to the patient and even the correlations between prescribed medication to the patient. To ensure efficiency and provide quality services, we will use queries on the data we collected to provide insight on how to improve the hospital's operations. 

## Data Model: 

Explanation of the data model: 

The data model is based off of how a hospital is potentially ran. Each entity represents either a hospital department (Doctor, Insurance, Billing, etc.) or a client that the hospital takes (Insurance, Patient, Appointment, etc.). 

At the center of the data model, there is an entity labeled Doctor. Each doctor can be identified through their unique ID and has relevant information such as their names, department and years of experience in our database. For every doctor, there can be multiple appointments with patients. Each doctor can also have up to one multiple malpractice case. To the right of the Doctor entity, there is a separate entity called Patient. Each patient can have multiple doctors treat them and each doctor can treat multiple patients. This is shown by the table Patient_Has_Doctor, which holds data on when a patient is assigned a doctor and their discharge date. Each patient can also have multiple appointments and due to that they can have multiple Billing entries as well. 

For Insurance, one insurance policy can cover multiple patients' bills. Through the entity DoctoralCoverage, insurance has a many to many relationship with Doctor, meaning a doctor can accept multiple insurance policies and an insurance policy can be accepted by multiple doctors. 

A Nurse can attend to multiple patients and a patient can have multiple nurses. The nurses shift is recorded in the Patient_has_Nurse table. 

Lastly, we depect Medication records for each patient. The same medication can be prescribed to multiple patients and a patient can be prescribed various types of medication. The date a patient starts a certain medication is recorded in the table PatientMedication. 

<img width="791" alt="image" src="https://github.com/user-attachments/assets/43ce1d41-0f95-4a88-915c-900fc0244909">


## Data Dictionary: 

## Queries: 

## Database Information: 
