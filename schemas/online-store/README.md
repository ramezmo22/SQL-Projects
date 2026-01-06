📖 Overview
This project designs a relational database schema for an Online Store. It covers products, customers, orders, payments, shipping, and reviews. The goal is to organize store data clearly, support key e-commerce operations, and maintain data integrity.
🗂️ Main Tables
- Products: ProductID, Name, Description, Price, Stock, ImageURL
- Customers: CustomerID, Name, Email, Phone, Address, Username, PasswordHash
- Orders: OrderID, CustomerID, DateTime, TotalAmount, ShippingMethod, Status
- OrderDetails: OrderDetailID, OrderID, ProductID, Quantity, UnitPrice
- Payments: TransactionID, OrderID, CustomerID, Amount, Method, Timestamp
- Shipping: ShippingID, OrderID, Carrier, TrackingNumber, Status, EstimatedDate, ActualDate
- Reviews: ReviewID, ProductID, CustomerID, Text, Rating (1–5), Timestamp
🔗 Relationships
- Customers → Orders (One-to-Many)
- Orders → Products (Many-to-Many via OrderDetails)
- Orders → Payments (One-to-One)
- Orders → Shipping (One-to-One)
- Customers → Reviews → Products (Many-to-Many)
