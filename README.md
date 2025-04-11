# SQL User Authentication System

This project implements a basic user authentication system with access logging capabilities. It includes scripts to create tables for storing user credentials and tracking user access.

## Database Setup

```sql
-- Create the database
CREATE DATABASE Practical15;
GO

-- Use the database
USE Practical15;
GO
```

## Table Structure

### Users Table

The Users table stores authentication credentials.

```sql
CREATE TABLE Users (
    Id INT PRIMARY KEY IDENTITY(1,1),
    Username NVARCHAR(100) NOT NULL,
    Password NVARCHAR(100) NOT NULL
);
```

### AccessLogs Table

The AccessLogs table tracks user login activity.

```sql
CREATE TABLE AccessLogs (
    Id INT PRIMARY KEY IDENTITY(1,1),
    UserName NVARCHAR(100),
    AccessTime DATETIME
);
```

## Initial Data

The system comes pre-populated with test user accounts:

```sql
INSERT INTO Users (Username, Password)
VALUES 
('admin', 'admin123'),
('user1', 'user123'),
('user2', 'pass456');
```
