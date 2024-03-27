# MIST4610GroupProject1
## Team Name:
21484 Group 2
## Team Members
1. Kush Santosh [@kushsantosh](https://github.com/kushsantosh)
2. Megan Aldinger @meganaldinger
3. Patrick Daws [@PatrickD93](https://github.com/PatrickD93)
4. Priya Dey [@priyaadey](https://www.github.com/priyaadey)
5. Lucy Moon [@lucymoon505](https://github.com/lucymoon505/4610GroupProject1)
6. Ansley Williams [@ansleymw](https://github.com/ansleymw/ansley4610)

## Problem Description:
Our task at hand was to model and build a relational database system for an emergency healthcare clinic chain. At the core of this model is the Patient entity of the healthcare clinic, representing each new individual checked into the hospital as a patient. There are multiple patients in many different countries and cities. The database includes many different relationships with the patient, including prescription information and billing details. Information about patient appointments and their corresponding diagnostic tests are also available, along with additional detail about these scans. Our goal is to accurately model these relationships to swiftly deliver precise patient information, crucial in high-stakes environments like emergency healthcare clinics. Furthermore, we aim to enable seamless querying of this data, empowering doctors, nurses, and healthcare professionals with vital insights into doctor-patient relationships and the hospital's operational dynamics.
## Data Model:
Our data model represents an emergency healthcare clinic chain. We have thirteen entities connected by one-to-many and many-to-many relationships. We have a patient entity that holds attributes such as their name, contact information, date of birth, and medical history. Patient has a one-to-many relationship with three different entities: Bill, Appointment, and Prescription. A patient can have many bills from the clinic (that include the total amount owed, payment status, etc), and a patient can have multiple prescriptions prescribed. Each prescription includes the name of the medicine and the dosage. Multiple prescriptions are in one pharmacy, which is displayed by the one-to-many relationship between the Prescription and Pharmacy entities. Pharmacy attributes include where it is located, the contact information, and the name of the manager. 
	
 One patient can have many appointments at the clinic. Appointment stores which patient is associated with the appointment, which medical staff is associated with the appointment, the date of the appointment, the reason for the visit, and its unique identifier. One appointment can have many diagnostic tests, which store the type of test, results of the test, which staff is involved, and which laboratory it took place in. In order to show where the diagnostic test takes place, there is a Laboratory entity connected as a one-to-many relationship with the Diagnostic Test entity. Laboratory holds attributes such as where the lab is, the lab phone number, and the lab manager. An appointment can also have many medical diagnoses. The MedicalDiagnosis entity holds when the diagnosis took place, and the professional’s assessment. Appointment also has a many-to-many relationship with the MedicalEquipment entity (which includes type of equipment, and equipment quantity). This is an identifying relationship, and it has an associative entity called ScansAndEvaluations, which holds the foreign keys of MedicalEquipment and Appointment.
	
 One medical staff can have many appointments, and can perform many diagnostic tests. Information stored in the MedicalStaff entity include the name of the staff member, their specialization, and their contact information. Many medical staff can be in one training session, which includes the training session topic and date. Many medical staff are on one staff schedule, and the staff schedule entity holds the schedule date attribute. 


![Screenshot 2024-03-27 at 11 49 23 AM](https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/2e132544-6932-4d3f-bd57-877dcddf2abb)

## Data Dictionary:
![Screenshot 2024-03-26 at 9 38 01 PM](https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/8f0382fa-f72a-4d10-9e5f-a650846edfd3)

![Screenshot 2024-03-26 at 9 38 19 PM](https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/9d8106fe-5dad-4456-ba6b-bf26b3e21a69)

![Screenshot 2024-03-26 at 9 40 21 PM](https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/ff37ea51-6e4d-4aa0-b318-d1d5308d9e99)

![Screenshot 2024-03-26 at 9 40 30 PM](https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/d1f8eee5-a7ab-4034-a777-2cd4e51eda67)

![Screenshot 2024-03-26 at 9 40 51 PM](https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/feb76c6f-329d-44ad-b723-501b700fda51)

![Screenshot 2024-03-26 at 9 41 14 PM](https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/3f903b65-736c-4c29-8566-41f38991c916)

![Screenshot 2024-03-26 at 9 41 44 PM](https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/a5cac6b1-30b9-4718-80f5-21c2dc829cef)

![Screenshot 2024-03-26 at 9 41 59 PM](https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/a9d51e54-3c13-47b6-97f0-4388feca79d9)

![Screenshot 2024-03-26 at 9 43 00 PM](https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/fc2fd9f1-83af-4105-9de0-da0cb358d8fd)

![Screenshot 2024-03-26 at 9 43 14 PM](https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/11c1bfd3-f60d-4249-9307-a8afe403e336)

![Screenshot 2024-03-26 at 9 43 33 PM](https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/41055d83-acda-4f17-893f-71561c271228)

![Screenshot 2024-03-26 at 9 43 49 PM](https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/22c4cf26-011b-407b-b054-dd522fa3642b)

![Screenshot 2024-03-26 at 9 44 03 PM](https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/9e7dd1c0-bf55-4aa6-8d7f-f8806508e56e)

## Queries:
(Insert Query Chart)
(Insert Queries)

## Database Information
