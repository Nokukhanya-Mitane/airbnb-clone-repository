# airbnb-clone-repository
## 🏡 Project Overview This project is part of the ALX Software Engineering Program. The goal is to **recreate a simplified version of the AirBnB web application**, focusing on understanding the fundamentals of backend development and object-oriented programming in Python. The project will be developed in phases, starting with a command-line interface for managing AirBnB objects, and later expanding into a fully functional web application.
---
## 🎯 Project Goals - Understand and implement object-oriented programming in Python - Build a command-line interface (CLI) for managing AirBnB data - Create custom classes and handle serialization/deserialization - Transition the project to use storage engines (File and DB) - Eventually develop a web interface for the application
---
## 🧰 Tech Stack - **Language:** Python 3.8+ - **Storage:** File storage (JSON), SQL (later stage) - **Frameworks:** Flask (web development in later stages) - **Tools:** Git, Unit Testing, Command Line 
---
## 🚀 Getting Started To get started:
bash
git clone https://github.com/YOUR-USERNAME/airbnb-clone-project.git

## Team Roles

The AirBnB Clone project involves multiple roles, each with specific responsibilities to ensure smooth development and delivery:

- **Backend Developer**  
  Designs and implements the server-side logic, APIs, and core application functionality. Responsible for data processing and business rules.

- **Database Administrator (DBA)**  
  Manages database design, optimization, data integrity, and migrations. Ensures efficient and secure data storage and retrieval.

- **QA Engineer**  
  Creates and executes test plans to ensure software quality. Responsible for identifying bugs and verifying fixes through automated and manual testing.

- **DevOps Engineer**  
  Automates deployment processes, manages CI/CD pipelines, and maintains the infrastructure for reliable application delivery.

- **Frontend Developer**  
  Develops the client-side interface using HTML, CSS, and JavaScript. Connects UI elements with backend APIs to create interactive user experiences.

- **Project Manager**  
  Coordinates project tasks, manages timelines, facilitates communication among team members, and ensures project goals are met.

- **Research & Documentation Lead**  
  Collects technical information, writes documentation, and maintains project knowledge to help the team stay aligned and informed.

> *Note: Roles may overlap or evolve based on project phases and team size.*

## 🧰 Technology Stack This project uses a range of modern technologies to build and manage the backend functionality of the AirBnB Clone. Below is an overview of the key technologies and their roles in the project:
| Technology | Purpose |
|----------------|-------------------------------------------------------------------------|
| **Python** | The core programming language used for writing all backend logic and modules. | 
| **Flask** | A lightweight Python web framework used to create RESTful APIs and manage server-side routing (used in later phases). |
| **MySQL** | A relational database system used for storing persistent data such as users, places, and bookings. | 
| **SQLAlchemy** | An Object Relational Mapper (ORM) that helps interact with the MySQL database using Python objects instead of SQL queries. |
| **HTML/CSS** | (Frontend - Later Phase) Used to structure and style the web interface of the application. | 
| **JavaScript** | (Frontend - Later Phase) Adds interactivity to the UI and communicates with backend APIs. |
| **Git** | Version control tool used to track changes, manage branches, and collaborate as a team. |
| **GitHub** | Remote repository hosting platform for code collaboration and project documentation. | 
| **Unittest** | Python’s built-in testing framework used to write and run test cases to ensure code quality. |

## 🗃️ Database Design
The database for the AirBnB Clone project is designed to manage users, properties, bookings, reviews, and payments efficiently. Below is an overview of the key entities and their fields, along with the relationships between them.
# 🧑‍💼 1. Users Represents users of the platform including hosts and guests. **Key Fields:** - `id` (Primary Key) - `name` - `email` - `password_hash` - `user_type` (host or guest)
---
# 🏠 2. Properties Represents the listings or accommodations available for booking. **Key Fields:** - `id` (Primary Key) - `user_id` (Foreign Key → Users) - `title` - `description` - `location` - `price_per_night`
--- 
# 📅 3. Bookings Captures booking details made by guests for a property. **Key Fields:** - `id` (Primary Key) - `user_id` (Foreign Key → Users) - `property_id` (Foreign Key → Properties) - `check_in_date` - `check_out_date` - `total_price`
--- 
# 🌟 4. Reviews Allows users to leave feedback on properties. **Key Fields:** - `id` (Primary Key) - `user_id` (Foreign Key → Users) - `property_id` (Foreign Key → Properties) - `rating` (1–5) - `comment` 
---
# 💳 5. Payments Tracks transactions for bookings. **Key Fields:** - `id` (Primary Key) - `booking_id` (Foreign Key → Bookings) - `amount` - `payment_method` - `payment_status` 
---
