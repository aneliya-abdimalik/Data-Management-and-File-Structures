# CENGFACTORYDB – JDBC Factory Database Manager

## Overview

This project implements a relational database manager using **Java JDBC** for a fictional manufacturing ecosystem called **CengFactory**. It provides full data management capabilities for factories, products, employees, and their relationships.

Developed for the **CENG 351: Data Management and File Structures** course at METU, this system connects to a **MySQL database**, creates required tables, inserts records, performs complex queries, and supports analytical operations over production, shipments, and employee data.

## Technologies Used

- Java 14
- JDBC (Java Database Connectivity)
- MySQL (remote server)
- SQL (DDL and DML queries)

## Schema

| Table      | Fields |
|------------|--------|
| Factory    | factoryId, factoryName, factoryType, country |
| Employee   | employeeId, employeeName, department, salary |
| WorksIn    | factoryId, employeeId, startDate             |
| Product    | productId, productName, productType          |
| Produce    | factoryId, productId, amount, productionCost |
| Shipment   | factoryId, productId, amount, pricePerUnit   |

## Tasks Implemented

- ✅ Create/drop all database tables
- ✅ Insert data into all tables via `.txt` files
- ✅ Retrieve factories by country
- ✅ Identify factories with no employees
- ✅ Find factories producing all products of a given type
- ✅ List products produced but not shipped
- ✅ Calculate average salary for a factory/department
- ✅ Compute most profitable products per factory
- ✅ Compute top-profit factories per product
- ✅ Find underpaid employees by department
- ✅ Increase production cost by a percentage
- ✅ Delete inactive employees by date

## Extra Features 

Implemented as methods:
- Employee salary ranking (dense/gap)
- 4th most profitable product per factory
- Salary variance by start date
- Auto-delete losing products from Produce table

