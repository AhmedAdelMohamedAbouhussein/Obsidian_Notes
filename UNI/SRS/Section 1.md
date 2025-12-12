## **2. Requirements Identification and Stakeholder Analysis**

### **Understanding the Problem Statement**

Virgo Hospital is expanding rapidly and aims to modernize its operations by implementing a **Health Information Network**. One major part of this initiative is the **Outpatient Management Module**, which will digitize patient registration, doctor consultations, appointment scheduling, and billing.  
The goal is to increase operational efficiency, reduce paperwork, and improve patient satisfaction while maintaining security, accuracy, and high system availability.

---

## **1. Business Requirements**

Business requirements define the **high-level objectives** the hospital wants to achieve through the system.

|**No.**|**Business Requirement**|**Description**|
|---|---|---|
|**BR1**|Improve Patient Handling Efficiency|Automate outpatient registration, consultation, and billing to reduce waiting times and manual errors.|
|**BR2**|Centralized Health Information Access|Ensure all patient data (records, prescriptions, appointments) are stored digitally and can be accessed securely by authorized hospital staff.|
|**BR3**|Enhance Hospital Decision Making|Generate Management Information System (MIS) reports for administrators to make informed business and operational decisions.|

---

## **2. System Requirements**

System requirements describe the **functional and non-functional features** that the software system must provide to support the business goals.

|**No.**|**System Requirement**|**Description**|
|---|---|---|
|**SR1**|Patient Registration Module|The system must allow receptionists to register patients using Mini and Comprehensive registration forms.|
|**SR2**|Billing and Payment Integration|The system must generate bills for consultation, tests, and medicines, supporting both cash and credit card payments.|
|**SR3**|Secure Access Control|The system must include user authentication and authorization to protect patient confidentiality and prevent unauthorized access.|

---

## **3. User Requirements**

User requirements describe what specific users (e.g., doctors, receptionists, patients) need to do with the system.

|**No.**|**User Requirement**|**Description**|
|---|---|---|
|**UR1**|Receptionists can register patients|Receptionists must be able to input patient details and update or view records quickly.|
|**UR2**|Doctors can access patient records|Doctors must be able to view patient history, prescribe medications, and schedule follow-ups.|
|**UR3**|Patients receive printed bills|Patients should receive a printed or digital copy of their payment receipts and consultation summary.|

---

## **4. Project Stakeholders**

Stakeholders are individuals or groups who have an interest or influence in the project.  
They are classified as **primary** (directly using or affected by the system) or **secondary** (indirectly involved).

| **Stakeholder**                          | **Role / Interest**                                                                | **Stakeholder Type** |
| ---------------------------------------- | ---------------------------------------------------------------------------------- | -------------------- |
| **Patients**                             | Receive treatment, pay bills, and access their medical records                     | **Primary**          |
| **Doctors / Physicians**                 | Use the system to record diagnosis, prescribe medication, and view patient history | **Primary**          |
| **Receptionists**                        | Register patients and schedule appointments                                        | **Primary**          |
| **Billing / Accounting Staff**           | Handle patient billing, payment, and financial reporting                           | **Primary**          |
| **Hospital Administrators / Management** | Monitor system performance, view reports, and make business decisions              | **Secondary**        |
| **IT Department / System Developers**    | Develop, maintain, and secure the system                                           | **Secondary**        |
| **Laboratory Technicians**               | Access and update test results linked to outpatient records                        | **Secondary**        |
| **Pharmacy Staff**                       | Access prescriptions and dispense medicines                                        | **Secondary**        |
| **Investors / Board Members**            | Oversee hospital performance and return on technology investment                   | **Secondary**        |

---

### **Primary Stakeholders**

The **Primary Stakeholders** are those who directly interact with and rely on the Outpatient Management Module for daily operations:

- **Patients**
    
- **Doctors / Physicians**
    
- **Receptionists**
    
- **Billing Staff**
    

---

## **5. Stakeholder Map**

| **Stakeholder**                     | **Role/Responsibility**                                       | **Power** | **Interest** |
| ----------------------------------- | ------------------------------------------------------------- | --------- | ------------ |
| **Hospital Chairperson/Management** | Approves budget and oversees project implementation           | High      | Low          |
| **Doctors**                         | Provide diagnosis, prescribe medication, view patient history | High      | High         |
| **Receptionists**                   | Register patients, schedule appointments, manage billing      | Medium    | High         |
| **Patients**                        | Receive treatment, register, and pay bills                    | Low       | High         |
| **System Developers**               | Design, implement, and maintain the software                  | High      | Medium       |
| **Database Administrator (DBA)**    | Manages patient and medical data security                     | Medium    | Medium       |
| **Pharmacy/Billing Staff**          | Process medication and payment transactions                   | Low       | Medium       |
