# Peacock Group
## Members:
 1. 25048 NTWARI Deus
 2. 25918 INGABIRE NZARAMBA Ritha
 3. 26155 Ishimwe Mahoro Christianne 
 4. 26046 MABHYALA Wulsy
 5. 25514 HURUMA Innocent
 6. 24849 Nahayo Arnaud
 7. 25964 Mugisha Godefroid
 8. 26073 UMUGWANEZA Aimée
 9. 26975 NIYOYAVUZE AMIELLE PONTIENNE
 10. 25899 Arnaud NSHUTI
 11. 25444 Uwizeye Ngoga Sandra



# Police Examination Process - README

## Project Overview
The **Police Examination Process** project aims to develop a streamlined, digitalized system to support applicants in obtaining driving licenses, covering everything from registration to examination and result notification. Key processes are automated to minimize manual data handling and ensure data accuracy.

## Project Phases

### Phase 2: Business Process Modeling (BPMN Diagram)
- **Scope:** Design a digitalized driving license application process, from registration to final issuance.
- **Objectives:**
  - Reduce manual errors and enhance processing efficiency.
  - Automate notifications for exam scheduling and results.
- **Expected Outcomes:**
  - Improved data accuracy and faster processing.
  - Centralized database accessible by authorized departments.

- **Key Entities:**
  - **Applicant:** Applies for a license.
  - **Police Officer:** Verifies documents and approves applications.
  - **Examination Center:** Conducts exams and records results.
  - **License:** Issued upon successful completion.

- **Process Flow:** Application Submission → Document Verification → Exam Scheduling → Result Recording → License Issuance or Retest Notification.
- **Decision Points:** Includes checks like "Document Approved?" and "Exam Passed?"

- **Summary:** The process is centralized within a Management Information System (MIS), improving decision-making, efficiency, and reducing errors.

### Phase 3: Logical Model Design
- **Data Model Design:**
  - **Entities & Attributes:**
    - **Applicant:** `applicant_id (PK)`, `fname`, `lname`, `Date_birth`, `gender`, `address`.
    - **Application:** `application_id (PK)`, `applicant_id (FK)`, `application_date`, `status`, `remarks`.
    - **Examination Schedule:** `schedule_id (PK)`, `application_id (FK)`, `exam_date`, `exam_center_id (FK)`, `notification_status`.
    - **Examination Center:** `center_id (PK)`, `center_name`, `location`, `capacity`.
    - **Test:** `test_id (PK)`, `schedule_id (FK)`, `examiner_id (FK)`, `test_type`, `result`, `comments`.
    - **Examiner:** `examiner_id (PK)`, `fname`, `lname`, `qualification`, `assigned_center`.
    - **License:** `license_id (PK)`, `applicant_id (FK)`, `issue_date`, `expiration_date`, `license_type`.
    - **Notification:** `notification_id (PK)`, `schedule_id (FK)`, `sent_date`, `status`, `message_type`.

- **Relationships:**
  - **One-to-Many:** An applicant can have multiple exam attempts.
  - **One-to-One:** One result per exam.

- **Data Scenarios:**
  - **Failed Exam:** Track failed attempts and flag retest eligibility.
  - **License Issuance:** Issue a license upon passing and archive records.
  - **Notifications:** Automate exam schedule and result notifications.

## Conclusion
The **Police Examination Process** project establishes an efficient, digitalized workflow for driving license applications, with enhanced speed, accuracy, and centralized data management through BPMN modeling and structured data relationships.
