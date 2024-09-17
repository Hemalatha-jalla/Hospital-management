
Hospital Management System Database
This repository contains SQL scripts for creating and managing a database for a Hospital Management System. The database contains several entities, such as customers, reservations, menu items, staff, and billing sections, to handle various hospital-related operations efficiently. Each script is responsible for creating a specific table and inserting some initial data.

Table of Contents
Database Overview
Entities Overview
Independent Entities
Dependent Entities
Database Setup Instructions
File Structure
Sample Data
Database Overview
The Hospital Management System database consists of the following tables:

Customer - Stores information about hospital customers.
Reservation - Manages reservations (for services, rooms, etc.).
Menu - Contains details about items/services offered by the hospital (for example, hospital meals, medical services).
Staff - Manages hospital staff data, including positions and salaries.
Billing_Section - Handles billing and payment information.
Entities Overview
Independent Entities
Customer Table

Attributes:
C_ID (INT): Primary Key, Customer ID.
NAME (VARCHAR): Customer name.
PHONE_NUM (VARCHAR): Customer contact number.
NEEDS (VARCHAR): Special needs or preferences.
FEEDBACK (TEXT): Feedback provided by the customer.
Description: The Customer table stores basic information about patients or hospital service users.
Menu Table

Attributes:
M_ID (INT): Primary Key, Menu Item ID.
ITEM (VARCHAR): Name of the item or service.
PRICE (DECIMAL): Price of the item or service.
AVAILABILITY (VARCHAR): Availability status (e.g., available, out of stock).
TYPE (VARCHAR): Type of item/service (e.g., Main Course, Appetizer, etc.).
Description: The Menu table contains all the available services, food items, or treatments provided by the hospital.
Staff Table

Attributes:
S_ID (INT): Primary Key, Staff ID.
POSITION (VARCHAR): Job position (e.g., doctor, nurse, cleaner).
SALARY (DECIMAL): Salary of the staff member.
NAME (VARCHAR): Name of the staff member.
GENDER (VARCHAR): Gender of the staff member.
Description: The Staff table stores information about hospital personnel and their roles.
Dependent Entities
Reservation Table

Attributes:
R_ID (INT): Primary Key, Reservation ID.
C_ID (INT): Foreign Key, linked to the Customer table.
TABLE_NUM (INT): Assigned table/room number.
STATUS (VARCHAR): Status of the reservation (e.g., Confirmed, Cancelled, Waiting).
TIME (TIMESTAMP): Date and time of the reservation.
Dependencies: The Reservation table depends on the Customer table, with C_ID as a foreign key.
Billing_Section Table

Attributes:
B_ID (INT): Primary Key, Billing ID.
TOTAL_AMOUNT (DECIMAL): Total amount billed.
PAYMENT_MODE (VARCHAR): Mode of payment (e.g., Cash, Credit Card, Online).
DATE (DATE): Date of the transaction.
TAX (DECIMAL): Tax applied on the bill.
Dependencies: The Billing_Section table is linked to other tables like Customer (through the C_ID) and Reservation for the billing details.
