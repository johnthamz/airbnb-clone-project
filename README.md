## Airbnb-clone-project
This project is a simplified back-end clone of the AirBnB platform. It is part of the ProvDev Back-End Development training program.
## Project Goals
-Learn core back-end development principles
-Understand RESTful APIs and data models
-Practice Git and GitHub for version control
-Learn core back-end development principles
-Understand RESTful APIs and data models
-Practice Git and GitHub for version control
## Tech Stack
- Python
- Django
- PostgreSQL
- Git & GitHub


## Team Roles
Here are the key roles involved in the AirBnB Clone Project and their responsibilities:

### 1. Backend Developer
Responsible for building and maintaining the server-side logic. They create APIs, handle authentication, and ensure communication between the database and the front end.
### 2. Database Administrator (DBA)
In charge of designing, maintaining, and optimizing the database. Ensures data is stored securely, performs backups, and monitors performance.
### 3. DevOps Engineer
Handles deployment, CI/CD pipelines, and server management. Ensures the application runs smoothly in development, staging, and production environments.
### 5. Project Manager
Oversees the entire project, tracks progress, coordinates the team, and ensures deadlines and goals are met.
### 6. QA Engineer
Tests the application for bugs, usability issues, and performance problems. Ensures the final product is stable and reliable.


## Technology Stack

Here is a list of technologies used in the AirBnB Clone Project and their purpose:

### 1. Django
A high-level Python web framework used to build the back-end of the application. It helps handle routing, user authentication, and serves as the foundation for building RESTful APIs.

### 2. Django REST Framework (DRF)
An extension of Django that makes it easy to build powerful RESTful APIs. It handles common tasks like serialization, permissions, and viewsets.

### 3. PostgreSQL
A powerful open-source relational database used to store and manage structured data such as user profiles, property listings, bookings, and payments.

### 4. GraphQL
An alternative to REST APIs that allows the client to request exactly the data it needs. It makes queries more efficient and flexible.

### 6. Git & GitHub
Version control tools used to track changes in code and collaborate with team members. GitHub also hosts the project repository.


## Database Design

This project will use a relational database (e.g., PostgreSQL) to store structured data. Below are the key entities and their relationships.

### 1. Users
Represents individuals who can register and use the platform.

**Fields:**
- `id`: Unique identifier for the user
- `name`: Full name of the user
- `email`: Email address (used for login)
- `password`: Hashed password
- `role`: Type of user (e.g., host or guest)

### 2. Properties
Represents listings created by hosts that can be booked.

**Fields:**
- `id`: Unique identifier
- `title`: Name of the property
- `description`: Property details
- `location`: Address or city
- `price_per_night`: Cost per night

**Relationship:**
- A user (host) can own multiple properties

### 3. Bookings
Represents reservations made by users for specific properties.

**Fields:**
- `id`: Unique identifier
- `user_id`: The user who made the booking
- `property_id`: The property being booked
- `start_date`: Check-in date
- `end_date`: Check-out date

**Relationship:**
- A user can make multiple bookings
- A property can have many bookings

### 4. Reviews
Users can leave feedback on properties they have booked.

**Fields:**
- `id`: Unique identifier
- `user_id`: Reviewer’s ID
- `property_id`: Reviewed property
- `rating`: Numerical score (e.g., 1–5)
- `comment`: Text feedback

**Relationship:**
- A user can leave many reviews
- A property can have many reviews

### 5. Payments
Tracks transactions made for bookings.

**Fields:**
- `id`: Unique identifier
- `booking_id`: Booking this payment is for
- `amount`: Total payment amount
- `payment_date`: Date of transaction
- `status`: Payment status (e.g., completed, failed)

**Relationship:**
- Each booking can have one payment


## Feature Breakdown

Below is a list of the main features of the Airbnb Clone project and how they contribute to the overall functionality:

### 1. User Management
Allows users to register, log in, and manage their profiles. This is essential for authentication and tracking user activities such as bookings and property listings.

### 2. Property Management
Enables users (hosts) to create, update, delete, and view property listings. This forms the core of the platform, allowing accommodation options to be shared with potential guests.

### 3. Booking System
Provides functionality for guests to book properties for a specified duration. It manages check-in and check-out dates and ensures that booking data is stored and retrievable.

### 4. Payment Processing
Handles all financial transactions related to bookings. It ensures secure and smooth payment between guests and hosts.

### 5. Review System
Allows users to leave ratings and comments on properties they have stayed in. This helps build trust in the platform and informs future guests about property quality.


## API Security

Securing the backend APIs is a critical part of the Airbnb Clone project. Here are the key security measures that will be implemented:

### 1. Authentication
Only registered users will be able to access certain features through secure login mechanisms
 Prevents unauthorized access to user accounts and personal data.

### 2. Authorization
Permissions will be applied to ensure users only perform actions they are allowed to. Example, only a host can update their own property.  
Protects resources by restricting access based on user roles or ownership.

### 3. Rate Limiting
Limits the number of API requests a user or IP can make in a given period to prevent abuse or denial-of-service attacks.
Helps maintain system stability and prevents spamming or brute-force attacks.

### 4. Data Validation & Sanitization
All inputs from users will be validated and sanitized before being processed.  
Prevents common security vulnerabilities such as SQL injection or XSS (Cross-Site Scripting).

### 5. Secure Payment Handling
Payment data will be handled using secure protocols and trusted third-party payment gateways.  
Protects financial transactions and builds user trust.

### 6. HTTPS Enforcement
All communications will use HTTPS to ensure data is encrypted between the client and the server.  
Prevents man-in-the-middle attacks and ensures data integrity.


## CI/CD Pipeline

CI/CD stands for Continuous Integration and Continuous Deployment. It is a set of practices that automate the process of testing, building, and deploying code to ensure software is delivered quickly, safely, and reliably.

### Why CI/CD is Important:
- **Continuous Integration (CI):** Automatically tests and integrates code changes from multiple developers, helping catch bugs early.
- **Continuous Deployment (CD):** Automatically deploys new versions of the application to production or staging environments, reducing manual work and speeding up delivery.

### Tools We Can Use:
- **GitHub Actions:** Automates workflows such as running tests or deploying code whenever changes are pushed to the repository.
- **Docker:** Helps package the application with all its dependencies to ensure it runs consistently across different environments.

By using CI/CD, our Airbnb Clone project will maintain code quality and ensure that updates are delivered faster with fewer bugs.

