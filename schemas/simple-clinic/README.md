📖 Overview
This project designs a relational database schema for a Simple Clinic Management System. It covers patient records, doctors, appointments, medical prescriptions, and billing. The goal is to streamline clinic operations and maintain comprehensive patient care records.

🗂️ Main Tables
- Patients: PatientID, Name, DateOfBirth, Gender, Phone, Email, Address, BloodType, EmergencyContact
- Doctors: DoctorID, Name, Specialization, Phone, Email, LicenseNumber, HireDate
- Appointments: AppointmentID, PatientID, DoctorID, DateTime, Duration, Status, ReasonForVisit
- MedicalRecords: RecordID, PatientID, DoctorID, Date, Diagnosis, Notes, TreatmentPlan
- Prescriptions: PrescriptionID, RecordID, Medication, Dosage, Frequency, Duration, Instructions
- Billing: BillID, PatientID, AppointmentID, Amount, PaymentMethod, PaymentDate, Status

🔗 Relationships
- Patients → Appointments (One-to-Many)
- Doctors → Appointments (One-to-Many)
- Patients → MedicalRecords (One-to-Many)
- Doctors → MedicalRecords (One-to-Many)
- MedicalRecords → Prescriptions (One-to-Many)
- Appointments → Billing (One-to-One)
