Portfolio Management System
Description
This project is a Node.js-based web application featuring user authentication, role-based access control, and portfolio management. It allows administrators and editors to manage a portfolio of items with CRUD (Create, Read, Update, Delete) functionality.
open file with 
cd Final-web- 

Features
User Authentication: Secure login and registration with hashed passwords.
Role-Based Access Control:
Admin: Full control over items (create, update, delete).
Editor: Limited access (can only create items).
Portfolio Management:
Items include a title, description, and timestamps (created, updated, deleted).
CRUD operations for managing portfolio items.
User Dashboard: Displays items created by the logged-in user.
Admin Dashboard: Displays all items with management options.
Technologies Used
Backend: Node.js, Express.js
Frontend: EJS templates, CSS
Database: MongoDB
Authentication: bcrypt, express-session
Setup Instructions
Prerequisites
Node.js installed on your machine.
MongoDB instance running locally or in the cloud.
Environment Variables
Create a .env file in the project root and define the following:


PORT=3000
MONGODB_URL=url
Installation
Clone the repository:
bash

git clone https://github.com/AnniAnniA/final-back.git
cd portfolio-management
Install dependencies:
npm install
Start the server:
node index.js
The server will run at http://localhost:3000.
API Endpoints
Authentication
POST /register: Register a new user.
POST /login: Log in an existing user.
GET /logout: Log out the user.
Portfolio Management
GET /portfolio: View the portfolio page.
POST /admin/add-item: Add a new item (Admin only).
POST /admin/edit-item: Edit an existing item (Admin only).
POST /admin/delete-item/
: Delete an item (Admin only).
POST /editor/add-item: Add a new item (Editor only).
Dashboards
GET /dashboard: User dashboard showing their created items.
GET /admin: Admin dashboard showing all items.
GET /editor-dashboard: Editor dashboard for item creation.
Design Rationale
Security:

Passwords are hashed using bcrypt before storage.
Session-based authentication ensures secure user sessions.
Role-based middleware restricts access based on user roles.
Scalability:

Modular code structure allows for easy addition of new features.
MongoDB's schema flexibility supports dynamic updates.
User Roles:

Admin: Comprehensive control over items.
Editor: Limited to item creation.
How to Use
Register a User
Go to http://localhost:3000/register.
Fill in the registration form.
Login
Go to http://localhost:3000/login.
Enter your username and password.


