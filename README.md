# Team Unemployed MIST4610 Group Project 1

## Team Name: 
15058 Unemployed

## Team Members: 

1. Ben Lim [gituser](link)
2. Jason Roode
3. Jack Schaeffer
4. Yirong Shen [@Yishen6] (https://www.github.com/Yishen6)
5. Nathan To

## Problem Description: 

In order to provide the most efficient and organized method of patient intakes, we created a database showing the relationships between the various entities in a hospital environment. From taking in an appointment to seeing the actual patient, we strive to display how the hospital operates beyond what the patient experiences. To do this, we plan on using datamodels to show how the hospital staff work together, how billing and insurance relates to the patient and even the correlations between prescribed medication to the patient. To ensure efficiency and provide quality services, we will use queries on the data we collected to provide insight on how to improve the hospital's operations. 

## Data Model: 

Explanation of the data model: 

The data model is based off of how a hospital is potentially ran. Each entity represents either a hospital department (Doctor, Insurance, Billing, etc.) or a client that the hospital takes (Insurance, Patient, Appointment, etc.). 

At the center of the data model, there is an entity labeled Doctor. Each doctor can be identified through their unique ID and has relevant information such as their names, department and years of experience in our database. For every doctor, there can be multiple appointments with patients. Each doctor can also have up to one malpractice case. Malpractice cases are tracked in a separate entity and can be identified by idDoctor. 

To the right of the Doctor entity, there is a separate entity called Patient. Each patient can have multiple doctors treat them and each doctor can treat multiple patients. This is shown by the table Patient_Has_Doctor, which holds data on when a patient is assigned a doctor and their discharge date. Each patient can also have multiple appointments and due to that they can have multiple Billing entries as well. But, each Billing entry only belongs to one patient. 

For Insurance, one insurance policy can cover multiple patients' bills. Through the entity DoctoralCoverage, insurance has a many to many relationship with Doctor, meaning a doctor can accept multiple insurance policies and an insurance policy can be accepted by multiple doctors. 

A Nurse can attend to multiple patients and a patient can have multiple nurses. The nurses shift is recorded in the Patient_has_Nurse table. 

Lastly, we depect Medication records for each patient. The same medication can be prescribed to multiple patients and a patient can be prescribed various types of medication. The date a patient starts a certain medication is recorded in the table PatientMedication. 

Overall, the database revolves around the relationships between patients, doctors, nurses, appointments, medications and insurance. Many-to-many relationships are shown through bridge tables such as Patient_has_Doctor, Patient_has_Nurse, PatientMedication and DoctoralCoverage. 

![MIST4610 Project 1 Model](https://github.com/user-attachments/assets/cde60cd4-bfba-48b3-950e-96306b98ba1c)

## Data Dictionary: 

<img width="578" alt="image" src="https://github.com/user-attachments/assets/82e3ded6-e391-4723-8309-690ba17d937c">

<img width="581" alt="image" src="https://github.com/user-attachments/assets/b24be467-7df7-4b6e-87b0-5797a8ea6a5e">

<img width="583" alt="image" src="https://github.com/user-attachments/assets/795f19e9-523d-4d87-b393-c6771ff5b686">

<img width="582" alt="image" src="https://github.com/user-attachments/assets/c08eb15b-b3e7-44ca-a90e-d8ee4f884e75">

<img width="584" alt="image" src="https://github.com/user-attachments/assets/d928f264-b50c-49f2-83cb-ad4b79cc4ad8">

<img width="582" alt="image" src="https://github.com/user-attachments/assets/b1e6c39d-596d-458a-9977-52b0234daa58">

<img width="583" alt="image" src="https://github.com/user-attachments/assets/adef2803-4b6f-4ed3-85cb-d54eebb3bab8">

<img width="582" alt="image" src="https://github.com/user-attachments/assets/5e3b9afd-60cf-47ae-b191-c4c604d5eee4">

<img width="581" alt="image" src="https://github.com/user-attachments/assets/a855a2aa-9b8e-437e-9e13-f2f99b061efe">

<img width="583" alt="image" src="https://github.com/user-attachments/assets/84033ca0-71a5-435a-87d6-ee16d0c378b3">

<img width="580" alt="image" src="https://github.com/user-attachments/assets/524552dd-4bdf-4e0d-a638-d3de809d0362">

<img width="582" alt="image" src="https://github.com/user-attachments/assets/aa42e2bd-5cd3-47f2-90dd-b7840a53dabf">

## Queries: 

Insert Queries Table Here

Query 1: 

## Database Information: 

Name of Database: cs_ys69826

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();
