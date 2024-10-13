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

The data model is based off of how a hospital is potentially ran. It creates a comprehensive view of the medical system, insurance coverage, appointments, patient care, and relationships between doctors, nurses and patients. 

Starting on the upper left corner, we have an entity labeled **Insurance**. It holds attributes such as idInsurance, InsuranceName, PremiumAmount, and Coverage. These columns help us identify each individual insurance company a customer may be using and how much the insurance may be offering to cover. Insurance has two many to many relationships with Doctor and Patient. 

The relationship with Doctors create a third entity table named, **Network**. This is a weak entity with two foreign identifiers which are the primary keys of Insurance and Doctor. Each network is linked to an insurance policy while an insurance company can be in multiple networks. Each network is also linked to a specific doctor while one doctor can work with multiple networks. 

The biggest entity we have is the table representing **Doctor**. This entity holds the attributes idDoctor, Doctorfname, Doctorlname, Doctordept, YearsExperience, HeadDoctor, Specialiation, Email, and PhoneNumber. Besides the data to identify or contact a doctor, this table also holds information regarding a Head Doctor that can be in charge of multiple doctors. Specialization is also a foreign key from the entity Concentration. Doctor is also linked to Appointment and CareHistory. 

**Concentration** holds an identifier called idConcentration and ConcentrationName. A specific area of concentration can be practiced by multiple doctors. 

For every **Appointment** that is made, we note the idAppointment, Appointmentdate, Appointmenttime, idPatient, and idDoctor. Appointment is also a third entity created from the many to many relationship between Doctor and Patient. An appointment can involve only one patient and doctor at a time. Each appointment is made for one doctor but a doctor can have many appointments. Each appointment is also made for a specific patient but a patient can make multiple appointments. 

Another big entity we store data on is **Patient**. We record the idPatient, Patientfname, Patientlname, PatientAge, Gender, Email, PhoneNumber and DOB for every patient. Patient has many relationships with entities such as Patient_has_Nurse, PatientMedication, EmergencyContact, Billing and CareHistory. 

**CareHistory** is a weak entity made based of the many to many relationship between Doctor and Patient. A Doctor can have many listed care histories while each instance of care can only have one Doctor. Same with Patient where a patient can be treated multiple times but each listed history only has one patient. Every time care is given, it is possible for a patient to have a different doctor. CareHistory also records the AssignedDate and DischargeDate. 

Taking a look at the upper right corner, we have an entity called **Nurse**. This entity holds information on idNurse, Nursefname, Nurselname, HoursWorked, Email, and PhoneNumber. Nurses have a many to many relationship to patients, which creates a separate entity called **Patient_has_Nurse**. This weak entity is identified by both Patient and Nurse id. It also holds information such as ShiftStart and ShiftEnd to represent the working hours of the nurse. Each patient can have multiple nurses caring for them while each nurse can care for multiple patients. A nurse can only work on only one patient at a time. 



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
