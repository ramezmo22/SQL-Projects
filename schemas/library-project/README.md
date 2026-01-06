📖 Overview
This project designs a relational database schema for a Library Management System. It covers books, members, borrowing transactions, authors, categories, and staff management. The goal is to organize library operations efficiently and maintain accurate tracking of book loans and returns.

🗂️ Main Tables
- Books: BookID, Title, ISBN, PublicationYear, Edition, Quantity, AvailableCount, ShelfLocation
- Authors: AuthorID, Name, Biography, Nationality
- Categories: CategoryID, Name, Description
- Members: MemberID, Name, Email, Phone, Address, MembershipDate, Status
- Staff: StaffID, Name, Email, Phone, Role, HireDate
- BorrowTransactions: TransactionID, BookID, MemberID, BorrowDate, DueDate, ReturnDate, Status
- Fines: FineID, TransactionID, MemberID, Amount, Reason, IssueDate, PaymentDate, Status

🔗 Relationships
- Books → Authors (Many-to-Many via BookAuthors)
- Books → Categories (Many-to-Many via BookCategories)
- Members → BorrowTransactions (One-to-Many)
- Books → BorrowTransactions (One-to-Many)
- BorrowTransactions → Fines (One-to-One)
- Staff manages BorrowTransactions (One-to-Many)
