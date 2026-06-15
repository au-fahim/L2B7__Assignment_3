# ⚽ Football Ticket Booking System - Database Design & SQL Queries

## Overview
This project involves the design and implementation of a **Football Ticket Booking System** database. It tracks administrative staff and football fans, catalogs upcoming tournament matches, and manages individual ticket booking receipts. The project demonstrates core relational database concepts, including Entity-Relationship mapping, referential integrity, and complex SQL querying.

## Database Schema & Business Logic
The database architecture is built upon three primary tables:

1. **Users Table:** Manages registered users, restricting roles to either 'Ticket Manager' or 'Football Fan', and ensuring unique email addresses.
2. **Matches Table:** Catalogs tournament fixtures, categories, and base ticket prices, ensuring prices are non-negative and statuses are restricted (Available, Selling Fast, Sold Out, Postponed).
3. **Bookings Table:** A transactional table recording ticket purchases. It links users to specific matches, tracks payment statuses, and ensures total costs are logically calculated.

## Entity-Relationship Diagram (ERD)
The database structure relies on the following relationships:
* **One-to-Many:** One User → Many Bookings (A fan can buy tickets for multiple matches).
* **Many-to-One:** Many Bookings → One Match (A match receives thousands of bookings).
* **Logical One-to-One Mapping:** Each booking record explicitly links one specific user to one specific match.

> 🔗 **[View the Entity-Relationship Diagram on DrawSQL](https://drawsql.app/teams/auf-1/diagrams/football-ticket-booking-system-database-design)**

## Setup & Execution
To replicate and run this database environment locally:
1. Ensure you have a **PostgreSQL** environment configured.
2. Open the `QUERY.sql` file provided in this repository.
3. Run the entire script at once to drop existing tables, generate the DDL structures, seed the database, and execute the analytical queries.

---
