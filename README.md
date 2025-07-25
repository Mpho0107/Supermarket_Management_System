# 🛒 Supermarket Management System (CMPG311)

This is a relational database system designed to optimize operations in a modern supermarket. Developed using Oracle SQL, the system includes inventory tracking, payment processing, order handling, and customer data management. Built as part of the CMPG311 project.

---

## Team Members

- MP Thabane 
- MO Mbenyane 
- L Dube
- DE Masango 

---

## Table of Contents

- [Overview](#overview)
- [System Features](#system-features)
- [Entity Relationship Model](#entity-relationship-model)
- [Database Schema](#database-schema)
- [SQL Components](#sql-components)
- [Usage](#usage)
- [Indexes and Views](#indexes-and-views)
- [Installation & Tools](#installation--tools)
- [License](#license)

---

## Overview

The system automates supermarket operations such as:
- Inventory tracking and alerts
- Point-of-sale and payment processing
- Supplier and delivery management
- Sales reporting and compliance tracking

---

## System Features

- **Real-time inventory management** with restock alerts
- **Discount and pricing automation**
- **Employee access control**
- **Customer and supplier data tracking**
- **Financial reporting and fraud alerts**
- **Data encryption and GDPR-compliant storage**

---

## Entity Relationship Model

Entities include:

- `Customer`, `Order`, `OrderDetails`, `Payment`
- `Employee`, `Inventory`, `Product`, `Category`
- `Supplier`, `Brand`, `Discount`, `PaymentProcessor`
- `Supermarket`, `Shelf`, `Delivery`, `DeliveryService`

---

## Database Schema Overview

Sample tables:

```sql
CREATE TABLE Customer (
    CustomerID INT PRIMARY KEY,
    Name VARCHAR2(255),
    Address VARCHAR2(255),
    CellNumber VARCHAR2(20)
);

CREATE TABLE Product (
    ProductID INT PRIMARY KEY,
    Description VARCHAR2(255),
    CategoryID INT,
    BrandID INT,
    FOREIGN KEY (CategoryID) REFERENCES Category(CategoryID),
    FOREIGN KEY (BrandID) REFERENCES Brand(BrandID)
);

