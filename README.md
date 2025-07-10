# Aadhaar System Database Management Project

This project is a comprehensive database design and normalization solution for managing the Aadhaar system — a unique identification system in India. It involves designing an Entity-Relationship Diagram, converting it to a relational schema, identifying functional dependencies, and normalizing relations up to BCNF and 4NF where applicable.

## 📄 Project Overview

The goal of this project is to implement a normalized database for an Aadhaar enrollment and update system. It includes various modules such as:

- Citizen Information Management
- Enrollment Center Records
- Employee Management
- Aadhar Services (including Virtual ID and Biometric Locking)
- Appointments and Status Tracking
- Bank Account Linking
- Document Verification
- Online Service Usage

## 🗂️ Features

- Entity-Relationship (ER) Diagram
- Conversion to Relational Schema
- Functional Dependency Analysis
- Normal Forms (2NF → BCNF → 4NF)
- Decomposition of relations with multivalued dependencies
- Proper key identification for all relations

## 🧮 Tables and Key Relations

- `Citizen(CitizenNo, Fname, Mname, Lname, Gender, Locality, Pincode, State, DOB, EC_ID)`
- `EnrollmentCentre(EC_ID, EC_Name, EC_Type, Locality, Pincode, State)`
- `Employee(E_ID, Name, Email, PhoneNo, DepartmentName, EC_ID)`
- `RegisteredUser(AadharNo, CitizenNo, RegisteredMobileNo)`
- `AadharServices(VirtualID, LockStatus, EKYCStatus, BiometricLockStatus, AccountNo)`
- `Appointment(AppointmentID, Date, Time, AadharNo)`
- `AppointmentFor(AppointmentID, UpdateType, Status, EC_ID)`
- `Documents(DocumentType, AadharNo, DocumentSubmitted)`
- `BankAccount(AccountNo, IFSCCode, Name, Branch)`
- `OnlineCheckStatus(AadharNo, StatusType, Status)`
- `UpdateRequirement(UpdateType, UpdateFee)`
- `UpdateDocument(UpdateType, Document)`
- `AllStatus(StatusType)`
- `AvailServices(VirtualID, AadharNo)`
- `Finds(CitizenNo, EC_ID, Pincode)`

## ✅ Normalization Highlights

- All relations analyzed for functional dependencies.
- Most relations are in **BCNF**.
- Relations with multivalued dependencies (e.g., `AadharServices`) are decomposed into **4NF**.
- Composite keys and primary key closures used for determining normal forms.

## 📌 Tools & Technologies

- Draw.io / Manual drawing for ER diagram
- SQL-style relational modeling
- PDF documentation
- Manual normalization analysis

## 📎 File Structure

- `FINAL_AadharSystem_ER_Relational_Normalization.pdf` – Contains the ER diagram, relational schema, functional dependencies, and normalization steps.

## 📚 Purpose and summary

This repository is a reference for students and DBMS practitioners aiming to learn:

- Designing a real-world database schema
- Functional dependency reasoning
- Applying normalization principles
 

---

