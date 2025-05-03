# airbnb-clone-project
## Overview
This project is a simplified clone of the AirBnB web application. It is part of a larger learning journey to master the fundamentals of full-stack web development. The goal is to understand and replicate key features of the AirBnB platform including user authentication, listing creation, booking, and reviews.

## Project Goals
- Practice back-end and front-end integration.
- Understand data modeling and relational databases.
- Build a RESTful API.
- Apply version control using Git and GitHub.
- Improve debugging and testing skills.

## Technology Stack

This project uses a selection of powerful backend and data-related technologies to ensure a secure, scalable, and efficient application. Below are the key technologies used and their roles:

### Django
A high-level Python web framework used for building the core of the application, including business logic, user authentication, URL routing, and RESTful API development.

### PostgreSQL
A robust, open-source relational database system used to store and manage structured data such as user accounts, listings, bookings, and reviews.

### GraphQL
An API query language that enables clients to request only the data they need, improving performance and reducing payload sizes compared to REST.

### Git & GitHub
Version control and source code hosting tools used to track changes, manage collaboration, and maintain a centralized repository for the project.

---

This backend-focused technology stack provides a strong foundation for building a reliable and extensible AirBnB clone application.


## Database Design

This section outlines the structure of the database by identifying key entities and their relationships. The goal is to model the core functionalities of the AirBnB platform such as user management, property listings, bookings, reviews, and payments.

### Entities and Key Fields

#### 1. Users
Represents the individuals who can use the platform either as guests or hosts.
- `id` (Primary Key)
- `username`
- `email`
- `password_hash`
- `is_host` (Boolean to distinguish between hosts and guests)

#### 2. Properties
Represents the accommodations listed by hosts.
- `id` (Primary Key)
- `user_id` (Foreign Key referencing Users)
- `title`
- `description`
- `location`
- `price_per_night`

#### 3. Bookings
Represents a reservation made by a user for a specific property.
- `id` (Primary Key)
- `user_id` (Foreign Key referencing Users)
- `property_id` (Foreign Key referencing Properties)
- `check_in_date`
- `check_out_date`
- `total_price`

#### 4. Reviews
Represents feedback submitted by users after a stay.
- `id` (Primary Key)
- `user_id` (Foreign Key referencing Users)
- `property_id` (Foreign Key referencing Properties)
- `rating` (e.g., 1 to 5 stars)
- `comment`

#### 5. Payments
Represents payment transactions for bookings.
- `id` (Primary Key)
- `booking_id` (Foreign Key referencing Bookings)
- `amount`
- `payment_date`
- `payment_status` (e.g., completed, pending, failed)

### Entity Relationships
- A **User** can list multiple **Properties** (One-to-Many).
- A **User** can make multiple **Bookings** (One-to-Many).
- A **Property** can have multiple **Bookings** (One-to-Many).
- A **Booking** is linked to one **User** and one **Property** (Many-to-One).
- A **Property** can have multiple **Reviews** (One-to-Many).
- A **User** can write multiple **Reviews** (One-to-Many).
- A **Booking** has one **Payment** (One-to-One).

---

This relational database model ensures data integrity, scalability, and supports all core operations needed for the platform.


## How to Run the Project
1. Clone the repository:

## Team Roles

The development of the AirBnB Clone Project involves collaboration among various team members, each contributing unique skills and responsibilities. Below are the primary roles and their functions within the project:

### 1. Backend Developer
Responsible for building the server-side logic and functionality. This includes developing RESTful APIs, managing user authentication, handling business logic, and integrating with the database.

### 2. Frontend Developer
Focuses on the user interface and user experience of the application. Uses HTML, CSS, JavaScript, and frontend frameworks like Bootstrap to create responsive and interactive pages.

### 3. Database Administrator (DBA)
Designs and manages the database structure. Ensures efficient data storage, retrieval, backup, and security. Collaborates closely with backend developers to optimize database performance.

### 4. DevOps Engineer
Manages the deployment, monitoring, and performance of the application. Responsible for CI/CD pipelines, server provisioning, and infrastructure as code to ensure seamless development and delivery.

### 5. UI/UX Designer
Creates wireframes, mockups, and design prototypes to ensure the product is visually appealing and user-friendly. Works closely with frontend developers to bring the design to life.

### 6. Project Manager
Oversees the project timeline, tasks, and team coordination. Ensures all team members are aligned with the project goals and deliverables are met on schedule.

### 7. Quality Assurance (QA) Engineer
Tests the application for bugs, usability issues, and performance bottlenecks. Writes test cases and automation scripts to ensure the stability and reliability of the system.

---

Each role is essential in delivering a high-quality, functional, and scalable AirBnB Clone application.
