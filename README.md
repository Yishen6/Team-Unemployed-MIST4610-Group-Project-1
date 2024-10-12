# Team Unemployed MIST4610 Group Project 1

## Team Name: 
15058 Unemployed

## Team Members: 

1. Ben Lim [gituser](link)
2. Jason Roode
3. Jack Schaeffer
4. Yirong Shen [@Yishen6](https://www.github.com/Yishen6)
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

![New Model](https://github.com/user-attachments/assets/4964daa2-7ced-4983-9c3b-64abd3741fc7)


## Data Dictionary: 

<img width="578" alt="image" src="https://github.com/user-attachments/assets/82e3ded6-e391-4723-8309-690ba17d937c">

<img width="580" alt="image" src="https://github.com/user-attachments/assets/e81305f9-2436-4534-b23d-2478e284cc08">

<img width="580" alt="image" src="https://github.com/user-attachments/assets/1f186705-522c-425a-973b-272c7842a373">

<img width="580" alt="image" src="https://github.com/user-attachments/assets/d656399f-8d1c-47d7-85ab-18bec6211b9d">

<img width="582" alt="image" src="https://github.com/user-attachments/assets/d770d854-03fc-40ba-ab53-ac041c5892ca">

<img width="580" alt="image" src="https://github.com/user-attachments/assets/2dd1ffbd-a815-446e-9095-492a56833b10">

<img width="582" alt="image" src="https://github.com/user-attachments/assets/927d55b0-346e-44ad-b2bb-041628cc1d7d">

<img width="580" alt="image" src="https://github.com/user-attachments/assets/260e649e-b353-43d9-b5bd-cee25491a895">

<img width="582" alt="image" src="https://github.com/user-attachments/assets/5d2376b1-97a9-4dee-8127-d9a63a6b3cc2">

<img width="581" alt="image" src="https://github.com/user-attachments/assets/38443938-aa73-4145-8edb-18b2f7ec65a5">

<img width="611" alt="image" src="https://github.com/user-attachments/assets/994a0a47-e829-440f-a41d-370b2f35210c">

<img width="610" alt="image" src="https://github.com/user-attachments/assets/7fe060a3-2252-4af6-b531-506e861bff1f">

<img width="609" alt="image" src="https://github.com/user-attachments/assets/7c36f8a5-c3a2-49f9-ba93-05642b44b41e">

## Queries: 

Insert Queries Table Here

Query 1: 

## Database Information: 

Name of Database: cs_ys69826

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();
