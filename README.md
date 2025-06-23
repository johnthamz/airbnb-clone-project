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

