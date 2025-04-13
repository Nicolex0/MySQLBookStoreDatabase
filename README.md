# MySQLBookStoreDatabase

A MySQL database designed to manage a bookstore's operations, including books, authors, customers, orders, and shipping. This project demonstrates skills in database design, SQL table creation, user role management, and query execution.

## Project Overview

The **BookStoreDatabase** is a relational database built in MySQL to store and manage data for a bookstore. It includes 15 tables to handle various aspects of bookstore operations, such as:

- **Books and Authors**: Track book details, authors, and their relationships.
- **Customers and Addresses**: Manage customer information and multiple addresses.
- **Orders and Shipping**: Record customer orders, order lines, shipping methods, and order history.

The database enforces data integrity with primary keys, foreign keys, and appropriate data types. User roles (`admin`, `employee`, `customer`) are set up to control access securely.

## Repository Structure

The repository contains the following files:

- `create_database.sql`: SQL script to create the `bookstore` database and all tables.
- `setup_users.sql`: SQL script to define user roles (`bookstore_admin`, `bookstore_employee`, `bookstore_customer`) and assign permissions.
- `insert_data.sql`: SQL script to populate the database with sample data for testing.
- `test_queries.sql`: SQL script with sample queries to demonstrate database functionality.

## Setup Instructions

To set up and use the database, follow these steps:

1. **Install MySQL**:
   - Ensure MySQL (version 8.0 or later) is installed on your system.
   - Verify you have access to a MySQL client (e.g., MySQL Workbench, command-line client).

2. **Create the Database**:
   - Run the `create_database.sql` script to create the `bookstore` database and its tables:
     
     `mysql -u root -p < create_database.sql`

3. **Set up user roles**:
   - Run the `setup_users.sql` script to create roles and sample users:

     `mysql -u root -p < setup_users.sql`
  
  - Sample users include (admin1), (employee1), and (customer1) with passwords specified in the script. Update passwords as needed for security.

4. **Insert Sample Data**:
  - Run the `insert_data.sql` script to populate the database with sample data:

     `mysql -u root -p < insert_data.sql`

5. **Test the Database**:
  - Run the `test_queries.sql` script to execute sample queries and verify functionality:
    
     `mysql -u root -p < test_queries.sql`

## Usage
- Administrators: Log in as `admin1` to manage the database schema, users, and all data.
- Employees: Log in as `employee1` to manage books, orders, and customer data (no schema changes).
- Customers: Log in as `customer1` to browse books and manage personal orders and addresses.
- Use the queries in `test_queries.sql` as a starting point to explore the database, such as listing books by author or calculating order totals.

## Contributing
This project is an assignment submission, but feedback is welcome! If you have suggestions for improving the schema, queries, or documentation, feel free to open an issue or submit a pull request.

## License
This project is for educational purposes and does not include a formal license.
