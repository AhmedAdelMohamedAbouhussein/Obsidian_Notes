## **1. Chosen Project Life Cycle Methodology and Description**

### **Chosen Methodology: Agile (Incremental) Model**
### **Reason for Choosing Agile:**

The **Agile (Incremental) Model** is chosen for developing the **Outpatient Management Module** of Virgo Hospital’s Health Information Network because of its flexibility, adaptability, and ability to deliver functional modules quickly while requirements continue to evolve.

### **Justification:**

1. **Changing and Volatile Requirements:**  
    The case study mentions that “requirements may turn out to be somewhat volatile.” Agile supports continuous requirement refinement through iterative development and feedback.
    
2. **Incremental Delivery:**  
    The system can be developed and delivered in parts — for example:
    
    - **Iteration 1:** Patient registration and mini form handling
    - **Iteration 2:** Doctor–patient record access and diagnosis module
    - **Iteration 3:** Appointment scheduling
    - **Iteration 4:** Billing and payment processing
        
3. **Stakeholder Involvement:**  
    Frequent collaboration with doctors, receptionists, and hospital administrators ensures that each iteration is aligned with real hospital workflows.
    
4. **Reduced Risk and Faster Feedback:**  
    Each version is tested and reviewed by users, minimizing risk and improving the system’s usability and accuracy.
    
5. **Flexibility and Maintainability:**  
    Since hospital systems may need continuous updates (e.g., new billing rules, insurance integrations, or regulatory changes), Agile supports ongoing modifications efficiently.
    

---

## **2. Requirements Engineering Activities (Based on the Diagram)**

### **Diagram Reference:**

`Elicitation → Analysis & Modeling → Specification → Validation → Management & Change`

These activities form the backbone of the requirement engineering process for the Outpatient Management Module.

---

### **1. Elicitation — Discovering the Needs**

**Description:**  
Requirements were gathered from multiple stakeholders such as doctors, receptionists, patients, and hospital administrators.

**Techniques Used:**

- Interviews with medical staff
- Brainstorming sessions
- Studying existing manual registration and billing processes

**Example (Outpatient Module):**

- Receptionists requested a **Mini Registration Form** for emergency cases.
- Doctors requested access to **patient medical history and diagnosis records**.
- Management required **billing integration** with hospital accounts.

---

### **2. Analysis & Modeling — Making Sense of Requirements**

**Description:**  
In this phase, the gathered requirements were analyzed for consistency, redundancy, and feasibility. Models such as use case diagrams and data flow diagrams were developed.

**Example (Outpatient Module):**

- Use case diagrams identified actors: _Receptionist_, _Doctor_, and _Patient_.
    
- Data flow diagrams showed information flow between registration, consultation, and billing processes.
    
- Requirements were categorized:
    
    - **Functional:** Patient registration, appointment scheduling, billing generation
    - **Non-functional:** Security, availability, and data confidentiality

---

### **3. Specification — Writing the Requirements Clearly**

**Description:**  
All requirements were formally documented in the **Software Requirements Specification (SRS)**.

**Example (Outpatient Module):**

- _Functional Requirement:_  
    “The system shall allow a receptionist to register new patients using a Mini or Comprehensive Registration Form.”
    
- _Non-Functional Requirement:_  
    “The system shall provide access to patient data only to authorized users with valid login credentials.”
    

---

### **4. Validation — Are We Building the Right Product?**

**Description:**  
Validation ensures that the documented requirements truly reflect stakeholder needs.

**Techniques Used:**

- Prototype demonstrations
    
- Requirement walkthroughs with medical staff
    

**Example (Outpatient Module):**  
A prototype of the **patient registration interface** was reviewed by receptionists. Based on feedback, fields were rearranged for faster data entry during emergencies.

---

### **5. Management & Change — Keeping Control**

**Description:**  
As hospital policies and medical procedures evolve, requirements may change. This stage ensures all changes are tracked and approved before implementation.

**Example (Outpatient Module):**  
After deployment, management requested an enhancement to **email digital copies of patient bills**. This change was logged, reviewed for feasibility, and then added to the next system update.

---

## **3. Training Needs for Each Stakeholder Class**

Effective use of the Outpatient Management Module depends on proper training for all stakeholder groups involved.  
Below are the **training needs by stakeholder type:**

|**Stakeholder**|**Training Needs**|**Purpose / Expected Outcome**|
|---|---|---|
|**Reception Executives**|- Using the registration system (Mini & Comprehensive forms)  <br>- Appointment scheduling  <br>- Generating patient bills and receipts|To ensure fast and accurate patient handling at the front desk|
|**Doctors / Physicians**|- Accessing and updating patient records  <br>- Entering diagnoses, prescriptions, and follow-up details  <br>- Viewing patient history|To allow doctors to efficiently manage consultations and maintain accurate digital medical records|
|**Laboratory Technicians**|- Receiving test requests digitally  <br>- Uploading results into the system|To ensure test data is seamlessly linked with patient records|
|**Hospital Administrators**|- Monitoring daily outpatient statistics  <br>- Generating MIS reports  <br>- Managing doctor schedules and resource allocation|To support management decisions and efficient hospital operations|
|**Billing Staff / Accountants**|- Using the billing module  <br>- Integrating payment methods (cash, card)  <br>- Generating financial summaries|To ensure accurate accounting and billing for outpatient services|
|**IT Support Staff**|- System maintenance and backups  <br>- User account management  <br>- Security and data recovery procedures|To maintain reliability, security, and uptime of the system|
|**Patients (Indirect Users)**|- Guidance on online appointment booking or patient portal (if available)|To enhance user satisfaction and reduce manual dependency|
