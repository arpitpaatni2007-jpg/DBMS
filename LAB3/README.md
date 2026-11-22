# DBMS Lab 3 – Transactions, PL/SQL & Database Security

## 📘 Overview

This folder contains my **Database Management Systems Lab 3 Practical Assignment**, based on database transactions, PL/SQL programming and database-side operations using PostgreSQL.

The practical uses a Hospital Management Database consisting of Patient, Appointment, Appointment Log, Treatment and Prescription tables.

The assignment focuses on implementing triggers, managing transactions using savepoints, creating stored procedures and developing cursor-based functions using PL/pgSQL.

---

## 🗄️ Database Schema

The practical uses the following five tables:

| Table | Description |
|---|---|
| patient | Stores patient details |
| appointment | Stores appointment and doctor details |
| appointment_log | Maintains appointment status change records |
| treatment | Stores patient diagnosis and treatment information |
| prescription | Stores prescribed medicines and dosage |

### Table Relationships

- Appointment is connected to Patient through `patient_id`.
- Appointment Log records changes made to Appointment.
- Treatment is connected to Appointment through `appointment_id`.
- Prescription is connected to Treatment through `treatment_id`.

---

## 📝 Topics Covered (4 Questions)

| Q. No. | Topic | SQL Concepts |
|---|---|---|
| Q1 | Status Change Audit Trigger | CREATE FUNCTION, CREATE TRIGGER, OLD, NEW |
| Q2 | Transactions and Savepoints | BEGIN, SAVEPOINT, ROLLBACK TO, COMMIT |
| Q3 | Stored Procedures | CREATE PROCEDURE, CALL, PL/pgSQL |
| Q4 | Cursor-Based Summary | Explicit Cursor, OPEN, FETCH, LOOP, CLOSE |

**Total Marks: 20**

---

## 💻 Practical Implementation

The practical work includes:

1. **Status Change Audit Trigger:** Creating a trigger function named `log_status_change` and a trigger named `trg_status_audit` to record appointment status changes automatically in the appointment_log table.

2. **Transactions and Savepoints:** Booking an appointment using a transaction, creating a savepoint, performing a mistaken update, rolling back to the savepoint and committing the correct appointment record.

3. **Stored Procedures:** Creating `register_patient` to insert patient details and `enter_treatment` to insert treatment and prescription records in a single procedure call.

4. **Cursor-Based Doctor Appointment Summary:** Creating `doctor_appointment_summary(doc_id)` using an explicit cursor to retrieve patient names, appointment dates, statuses and diagnoses for a particular doctor.

---

## 🛠️ Technologies Used

- **PostgreSQL** – Relational Database Management System.
- **SQL** – Database operations and queries.
- **PL/pgSQL** – PostgreSQL procedural language.
- **Database Triggers** – Automatic execution of database operations.
- **Transactions** – Maintaining data consistency using transaction control.

---

## 🎯 Learning Outcomes

Through this practical assignment, I gained experience in:

- Understanding database triggers and trigger functions.
- Using OLD and NEW records inside triggers.
- Maintaining database consistency through transactions.
- Using SAVEPOINT and ROLLBACK for partial transaction recovery.
- Creating and executing stored procedures.
- Understanding PL/pgSQL programming.
- Working with explicit cursors and row-by-row processing.
- Retrieving structured reports using database functions.

---

## 📁 Files Included

This folder contains the main practical report and supporting assignment files:

- `DBMS_Lab3_Arpit_Patni_2501730111.pdf` – Complete Lab 3 practical report.
- `LAB3.1.pdf` – Supporting practical assignment file.
- `LAB3.2.pdf` – Supporting practical assignment file.
- `LAB3.3.pdf` – Supporting practical assignment file.

---

## 👨‍💻 Student Details

**Name:** Arpit Patni  
**Roll Number:** 2501730111  
**Course:** B.Tech CSE (AI & ML)  
**Section:** A  
**University:** K.R. Mangalam University, Gurugram  
**Subject:** Database Management System (DBMS)  
**Lab:** 3 – Transactions, PL/SQL & Database Security

---

*This repository contains my academic practical work completed as part of the DBMS course.*
