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

The relationship with Doctors create a third entity table named, **Network**. This is a weak entity with two foreign identifiers which are the primary keys of Insurance and Doctor. An insurance plan can accept multiple doctors. A doctor can also accept to take multiple insurance policies. But each instance of a network must only accept a single insurance plan and doctor at one time. 

The biggest entity we have is the table representing **Doctor**. This entity holds the attributes idDoctor, Doctorfname, Doctorlname, Doctordept, YearsExperience, HeadDoctor, Specialization, Email, and PhoneNumber. Besides the data to identify or contact a doctor, this table also holds information regarding a department head that can be in charge of multiple doctors. Specialization is also a foreign key from the entity Concentration. Doctor is also linked to Appointment and CareHistory. 

**Concentration** holds an identifier called idConcentration and ConcentrationName. A specific area of concentration can be practiced by multiple doctors. 

For every **Appointment** that is made, we note the idAppointment, Appointmentdate, Appointmenttime, idPatient, and idDoctor. Appointment is also a third entity created from the many to many relationship between Doctor and Patient. An appointment can involve only one patient and doctor at a time. A doctor can see to multiple appointments and a patient can book multiple appointments. 

Another big entity we store data on is **Patient**. We record the idPatient, Patientfname, Patientlname, PatientAge, Gender, Email, PhoneNumber and DOB for every patient. Patient has many relationships with entities such as Patient_has_Nurse, PatientMedication, EmergencyContact, Billing and CareHistory. 

**CareHistory** is a weak entity made based of the many to many relationship between Doctor and Patient. A doctor can provide care to multiple patients and a patient can be treated by multiple doctors. However, each instance of care is recorded to only have a single patient and doctor simultaneously. CareHistory also records the AssignedDate and DischargeDate so we know the duration of the treatment time. 

An important entity created by a many to many relationship between Insurance and Patient is **Billing**. This table holds DateBilled, Deductible, CoPay, PaymentStatus and AmountBilled. From an accountign perspective, this table holds the data that we need to calculate how much profit the hospital is making. An insurance company can provide coverage for multiple patients and a patient can use an insurance plan multiple times. But for our books, we record each bill with only one insurance plan and one patient at a time. This way we can organize which services were covered and which may still be processing. 

Taking a look at the upper right corner, we have an entity called **Nurse**. This entity holds information on idNurse, Nursefname, Nurselname, HoursWorked, Email, and PhoneNumber. Nurses have a many to many relationship to patients, which creates a separate entity called **Patient_has_Nurse**. This weak entity holds information such as ShiftStart and ShiftEnd to represent the working hours of the nurse. A patient can be helped out by multiple nurses and a nurse can see to multiple patients. A nurse can only work on only one patient at a time. 

An individual entity we have to the is **EmergencyContact**. It holds the information regarding each patient's emergency contact. Their unique id is listed along with EmergencyFName, EmergencyLName, Relationship, Email, PhoneNumber and PatientID. A patient can have one emergency contact and each emergency contact is linked to one patient. 

Aside from patient care, we also have data regarding **Medication** that can be prescribed to patients. This entity holds idMedication, MedicationName, DosageMG, and Frequency. This entity also has a many to many relationship with patients that creates another weak entity called **PatientMedication**. Besides being identified by the foreign keys from Patient and Medication, it also holds the StartDate of each medication. A patient can take multiple medications and a specific kind of medication can be assigned to multiple patient. But each prescription is recorded to only hold the data of one patient and one type of medication at once. 

![New Model](https://github.com/user-attachments/assets/4964daa2-7ced-4983-9c3b-64abd3741fc7)


## Data Dictionary: 

<img width="578" alt="image" src="https://github.com/user-attachments/assets/82e3ded6-e391-4723-8309-690ba17d937c">

<img width="610" alt="image" src="https://github.com/user-attachments/assets/d28dee6e-a643-4133-9804-48d378b9e238">

<img width="580" alt="image" src="https://github.com/user-attachments/assets/1f186705-522c-425a-973b-272c7842a373">

<img width="580" alt="image" src="https://github.com/user-attachments/assets/d656399f-8d1c-47d7-85ab-18bec6211b9d">

<img width="618" alt="image" src="https://github.com/user-attachments/assets/145684ef-c362-4401-88aa-663651250383">

<img width="612" alt="image" src="https://github.com/user-attachments/assets/fdca2640-aee8-415c-b6b1-de304c0d44f5">

<img width="582" alt="image" src="https://github.com/user-attachments/assets/927d55b0-346e-44ad-b2bb-041628cc1d7d">

<img width="580" alt="image" src="https://github.com/user-attachments/assets/260e649e-b353-43d9-b5bd-cee25491a895">

<img width="582" alt="image" src="https://github.com/user-attachments/assets/5d2376b1-97a9-4dee-8127-d9a63a6b3cc2">

<img width="581" alt="image" src="https://github.com/user-attachments/assets/38443938-aa73-4145-8edb-18b2f7ec65a5">

<img width="613" alt="image" src="https://github.com/user-attachments/assets/cd4f1a51-e38d-4b27-822b-87699d998faf">

<img width="610" alt="image" src="https://github.com/user-attachments/assets/7fe060a3-2252-4af6-b531-506e861bff1f">

<img width="609" alt="image" src="https://github.com/user-attachments/assets/7c36f8a5-c3a2-49f9-ba93-05642b44b41e">

## Queries: 

Insert Queries Table Here

Query 1: Give the appointments that were scheduled between October 20th and October 27th. Show the appointment ID, date and time. Also show the full names of the patient and doctor that was involved in the appointment. 

<img width="1219" alt="image" src="https://github.com/user-attachments/assets/3c796dc7-1d65-47f4-b582-6d5d0939053c">

Query 2: Find and list the insurance companies that offer a copay lower than the average copay. List the insurance id, company name and a new column names "avgCoPay".

<img width="1202" alt="image" src="https://github.com/user-attachments/assets/4e47af3d-481c-4837-b820-8b6c3a1586eb">

Query 3: Give the patient's full name and the insurance company they are using that have "Pending" payment statuses. Also include the amount billed. 

<img width="1208" alt="image" src="https://github.com/user-attachments/assets/571efc08-c10b-49ae-adc0-8507a622696b">

Query 4: For each individual nurse, only show the nurses that worked more hours than the average hours worked for all nurses. Include shift length in hours. 

<img width="1205" alt="image" src="https://github.com/user-attachments/assets/b29f4eb2-b187-47e8-9329-c5103b3bbcc2">

Query 5: List the patients that listed their parents as emergency contacts. Provide their contact information. 

<img width="1200" alt="image" src="https://github.com/user-attachments/assets/7b4ec9ca-d308-4359-8c3e-85ac070ab673">

Query 6: Find the patients with appointments that have have the area code 404 or 678. 

<img width="1207" alt="image" src="https://github.com/user-attachments/assets/a6b2a2f5-12f7-4869-ab5f-2698f16d3512">

Query 7: Given a doctor's unique id, show the patients that they cared for. Include their assigned dates and the date the patient is discharged on. 

<img width="1206" alt="image" src="https://github.com/user-attachments/assets/8130ff60-ea36-40c8-8be2-b20754da6d7c">

Query 8: For each insurance company, calculate the number of patients they have completed payments for, the average copay and the total amount paid. Total amount paid can be calculated as the sum of Deductibles and Copay. 

<img width="1210" alt="image" src="https://github.com/user-attachments/assets/a4315432-351b-4419-bdb9-95e67b42f8b0">

Query 9:  

<img width="1209" alt="image" src="https://github.com/user-attachments/assets/f42dc742-3a47-43b2-8fea-1d8d48c52a51">

Query 10:

<img width="1208" alt="image" src="https://github.com/user-attachments/assets/bad7bfb7-ec75-49e8-b2c0-9c5d0cfbdf28">


## Database Information: 

Name of Database: cs_ys69826

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();
