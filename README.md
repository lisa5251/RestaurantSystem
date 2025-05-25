# Hackathon Project

## Overview
This project is a web-based application designed for managing restaurant orders. It includes different user roles such as waiters, managers, and chefs, each with specific functionalities. The application allows users to log in, view their orders, and manage order statuses.

## File Structure
- **index.php**: Main functionality for waiters, checking user roles and displaying order summaries for the current month.
- **login.php**: User authentication, allowing users to log in to the system.
- **manager_dashboard.php**: Dashboard for managers, providing relevant information and functionalities.
- **chef_dashboard.php**: Dashboard for chefs, allowing them to view and manage orders.
- **styles.css**: CSS styles for the project, defining the visual appearance of the web pages.
- **db/schema.sql**: SQL schema for the database, defining the structure of the database tables and relationships.
- **README.md**: Documentation for the project, explaining how to set it up and use it.

## Database Schema
The database schema is defined in `db/schema.sql` and includes the following tables:

1. **users**: Stores user information.
   - `id` (INT, PRIMARY KEY, AUTO_INCREMENT)
   - `username` (VARCHAR, UNIQUE)
   - `password` (VARCHAR)
   - `role` (ENUM: 'waiter', 'manager', 'chef')
   - `logged_in` (BOOLEAN)

2. **orders**: Stores order details.
   - `id` (INT, PRIMARY KEY, AUTO_INCREMENT)
   - `waiter` (VARCHAR, FOREIGN KEY referencing users.username)
   - `table` (VARCHAR)
   - `status` (ENUM: 'pending', 'ready')
   - `time` (DATETIME)
   - `date` (DATE)

## Setup Instructions
1. **Database Setup**:
   - Create a new database in your MySQL server.
   - Run the SQL commands in `db/schema.sql` to create the necessary tables.

2. **Configuration**:
   - Update the database connection settings in your PHP files as needed.

3. **Running the Application**:
   - Start your local server (e.g., XAMPP).
   - Access the application through your web browser at `http://localhost/hackathon`.

## Usage
- Users can log in using their credentials.
- Waiters can view their orders and their statuses.
- Managers and chefs have their respective dashboards for managing orders.

## Contributing
Feel free to contribute to this project by submitting issues or pull requests.