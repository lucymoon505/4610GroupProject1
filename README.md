# MIST4610GroupProject1
## Team Name:
21484 Group 2
## Team Members
1. Kush Santosh [@kushsantosh](https://github.com/kushsantosh)
2. Megan Aldinger [@meganaldinger](https://github.com/meganaldinger)
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
<img width="887" alt="Screenshot 2024-03-27 at 9 48 52 PM" src="https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/c194fe45-a63c-44a2-8a13-35b392fcf508">

1. Query 1 displays important prescription information for a patient (including multiple prescription occurrences for a patient). It lists patient's names, pharmacy IDs, medicines, dosages, and prescription IDs.

<img width="1548" alt="Screenshot 2024-03-27 at 2 47 40 PM" src="https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/fe734322-bbdf-4500-abe7-9f0e0cc37b98">

This information can be used to identify the pharmacy the patient regularly goes to, making it easy for places like this clinic to transfer details. It also displays a patient’s prescription IDs, medicine, and dosage. These details make it convenient for clinic doctors in case of an emergency. They are easily able to view their patients’ pre-existing prescriptions and medication dosages before administering any other treatments, in case of potential complications.

2. Query 2 displays the past appointment and corresponding billing information for patients. It lists patient IDs, reasons for visiting, appointment IDs, bill IDs, and the total amount they spent.

<img width="679" alt="Screenshot 2024-03-27 at 2 55 12 PM" src="https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/741445d2-6033-423c-9766-c8280d786328">

This would be helpful to gather data about why patients visit and how much they spend each visit. 

3. Query 3 displays the full name of the staff member, their specialization, and the day they are scheduled to work if that employee specializes in either surgery or obstetrics.

<img width="821" alt="Screenshot 2024-03-27 at 2 57 19 PM" src="https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/dff25d2f-2036-4e39-8293-777efee8c0a9">

This query is useful to see what days employees who specialize in surgery or obstetrics are working in the clinic. This important data can be used to see which days on the schedule do not have a staff member who specialize in either of the aforementioned subjects. These scheduled days can be used to coordinate an appropriate appointment day with potential patients trying to come into the clinic for either surgery work or to be looked at by an obstetrician.

4. Query 4 displays the patient names (concatenated and aliased as patientName) and their total bill amount for all customers who have a diagnosis of any type of cancer (lung cancer, throat, etc.). It also orders by the total amounts from highest to lowest so that the organization can prioritize their funds to help the patients in the most financial distress.

<img width="908" alt="Screenshot 2024-03-27 at 3 00 45 PM" src="https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/1633d45d-fd08-494d-a322-8559a7eef4d7">

This query could be useful for the medical clinic who is partnering with an organization that is fundraising to pay the bills of patients with a specific illness. 

5. Query 5 returns concatenated patient first and last names and dosage quantity of patients where their dosage is greater than the average dosage prescribed for the patients whose birthday is in the 2000’s.

<img width="802" alt="Screenshot 2024-03-27 at 3 02 36 PM" src="https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/7a6a74e5-0919-44c7-be4f-5184fe15cb93">

This query is relevant and useful because the emergency room might want to monitor medical details for patients who are younger but taking higher dosages of medication than average. It can also help to pinpoint individuals who may need their dosages to be changed due to concerns with age. 

6. Query 6 displays the patients and the number of appointments where the amount they spent was greater than the average bill amount.

<img width="1125" alt="Screenshot 2024-03-27 at 9 16 15 PM" src="https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/e2a3072c-35a0-4fc8-acd4-221a06ccf93b">

This query is useful because it an help management identify patients who have spent large amounts of money to determine ways to reduce spending by seeing what is costing patients the most. 

7. Query 7 displays the different reasons people may be visiting the clinic and the percentage of patients that tested positive for each of those reasons. 

<img width="1627" alt="Screenshot 2024-03-27 at 9 19 55 PM" src="https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/a8fa4b8f-2d18-4611-980a-0078aa78452b">

This query is useful because it would allow the clinic to allocate resources and staff to properly address certain conditions. If people test positive they likely will have return visits, and it will also help the clinic to know where they can help with informing people about prevention of diseases where it’s most prevalent.

8. Query 8 displays the date on the staff schedule and the number of employees working that day when there is less than three people scheduled to work.

<img width="795" alt="Screenshot 2024-03-27 at 9 22 41 PM" src="https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/68eae441-4be5-4cb0-8235-55a62c21ec5a">

This query shows the dates on the staff’s schedule where there are less than three employees to work in the clinic that day. This is an important number because it tells upper management, who design the staff schedule, to assign more employees to the appropriate days to ensure the clinic is fully staffed and every patient is properly cared for. 

9. Query 9 displays the patient ID, patient name, the total amount they have spent, and the percentage of this amount out of the total amount spent by patients in Georgia.

<img width="1600" alt="Screenshot 2024-03-27 at 9 52 55 PM" src="https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/94e48389-355c-45ba-ab1b-d3021ef13402">

This can be used to identify which patients in Georgia are spending the most amount of money and how much they contribute to the total amount.

10. Query 10 retrieves the names of labs and diagnostic test times. It additionally filters by a specific test time.

<img width="1560" alt="Screenshot 2024-03-27 at 9 30 11 PM" src="https://github.com/kushsantosh/MIST4610GroupProject1Team2/assets/165107122/31127671-ac14-45b9-95cb-fd4deee065d8">

This query would be useful for a district lab manager who works for the healthcare clinic, and would like to analyze a trend in certain tests being done at different points in the year, improving practices by allocating resources accordingly, etc. 

## Database Information

Name of Database: ns_Sp24_21484_Group2

Procedure Call: CALL TP_Q1 ();
