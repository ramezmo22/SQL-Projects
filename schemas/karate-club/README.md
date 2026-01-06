📖 Overview
This project designs a relational database schema for a Karate Club Management System. It covers members, instructors, belt ranks, training sessions, competitions, and fee management. The goal is to organize club activities and track member progress efficiently.

🗂️ Main Tables
- Members: MemberID, Name, DateOfBirth, Gender, Phone, Email, Address, JoinDate, BeltRank, Status
- Instructors: InstructorID, Name, Phone, Email, BeltRank, Specialization, HireDate
- BeltRanks: RankID, RankName, Color, Level, RequiredTrainingHours
- TrainingSessions: SessionID, InstructorID, Date, StartTime, EndTime, Type, Capacity
- Attendance: AttendanceID, SessionID, MemberID, Date, Status
- Competitions: CompetitionID, Name, Date, Location, Type, Description
- CompetitionParticipants: ParticipantID, CompetitionID, MemberID, Category, Result, Award
- Fees: FeeID, MemberID, Amount, DueDate, PaymentDate, Status, Type

🔗 Relationships
- Members → BeltRanks (Many-to-One)
- Members → Attendance → TrainingSessions (Many-to-Many)
- Instructors → TrainingSessions (One-to-Many)
- Members → CompetitionParticipants → Competitions (Many-to-Many)
- Members → Fees (One-to-Many)
