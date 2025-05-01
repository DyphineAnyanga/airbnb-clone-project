## About the Project
The Airbnb Clone Project is a full-stack web application that simulates the functionality of the Airbnb platform. This real-world inspired project emphasizes backend systems, database design, API security, and CI/CD pipelines. It helps learners understand scalable architectures and collaborative workflows through hands-on development.

## Project Goals
- Understand full-stack web application structure.
- Apply modern software development practices.
- Collaborate using GitHub and team documentation.
- Implement database and API security best practices.
- Design and manage CI/CD pipelines.
- Integrate Django, MySQL, GraphQL, and Docker technologies.

## Technology Stack
- **Django*
- **MySQL*
- **GraphQL*
- **Docker*
- **GitHub Actions*

## Team Roles
### Backend Developer
Responsible for implementing business logic, setting up RESTful or GraphQL APIs using Django, and ensuring that the application runs as expected on the server side.
### Database Administrator (DBA)
Designs and manages the MySQL database, ensuring data integrity, optimization, and appropriate relationships between entities.
### DevOps Engineer
Sets up CI/CD pipelines using tools like GitHub Actions and Docker, ensuring smooth code integration, testing, and deployment processes.
### Frontend Developer
Integrates backend APIs with the user interface, manages client-side logic, and ensures a seamless user experience.
### Project Manager
Oversees project timelines, coordinates tasks among team members, ensures documentation is up to date, and aligns team output with the overall project goal.

## Technology Stack
- **Django**: Web framework used to build robust and scalable backend APIs and handle routing and business logic.
- **MySQL**: Relational database management system to store structured data such as users, bookings, and properties.
- **GraphQL**: A query language for APIs that enables efficient data retrieval and better frontend-backend communication.
- **Docker**: Containerization platform used to package the app for consistent deployment across environments.
- **GitHub Actions**: CI/CD tool for automating workflows such as testing, building, and deploying the application.

 ## Database Design
 
### Entities and Fields

- **User**
  - id (Primary Key)
  - name
  - email
  - password
  - role (guest, host)

- **Property**
  - id (Primary Key)
  - user_id (Foreign Key)
  - title
  - description
  - location

- **Booking**
  - id (Primary Key)
  - user_id (Foreign Key)
  - property_id (Foreign Key)
  - start_date
  - end_date

- **Review**
  - id (Primary Key)
  - user_id (Foreign Key)
  - property_id (Foreign Key)
  - rating
  - comment

- **Payment**
  - id (Primary Key)
  - booking_id (Foreign Key)
  - amount
  - payment_method
  - payment_status

### Relationships
- A **user** can list multiple **properties**.
- A **booking** is linked to one **property** and one **user**.
- A **review** is submitted by a **user** for a **property**.
- A **payment** is linked to a specific **booking**.


## Feature Breakdown

- **User Management**  
  Allows users to register, log in, and manage profiles. Supports different roles such as guests and hosts.

- **Property Management**  
  Hosts can create, update, or delete property listings. Listings include descriptions, images, and availability.

- **Booking System**  
  Guests can view properties, select dates, and make bookings. The system ensures availability and handles scheduling conflicts.

- **Review System**  
  After completing a stay, guests can leave reviews with star ratings and comments for properties.

- **Payment Integration**  
  Handles secure payment processing for bookings, ensuring successful and verifiable transactions.


## API Security

- **Authentication**: Secure login using JWT (JSON Web Tokens) to ensure that users are verified before accessing protected routes.

- **Authorization**: Role-based access control to restrict users from performing actions outside their permissions (e.g., only hosts can create listings).

- **Rate Limiting**: Prevents abuse by limiting the number of API requests per user/IP over time.

- **Data Validation and Sanitization**: Ensures that all inputs are checked and cleaned to prevent SQL injection, XSS, and other attacks.

**Why Security Matters:**
- **User Data Protection**: Keeps personal information such as emails and payment info secure.
- **Business Integrity**: Prevents unauthorized changes to listings and transactions.
- **Payment Security**: Protects against fraud during transactions.


## CI/CD Pipeline

**What is CI/CD?**  
CI/CD stands for Continuous Integration and Continuous Deployment. It automates the process of testing, building, and deploying applications, ensuring faster and safer releases.

**Tools Used:**
- **GitHub Actions**: To automate testing and deployment on every commit.
- **Docker**: To containerize the application for consistent environments across development, staging, and production.

**Benefits:**
- Reduces manual errors.
- Enables rapid iteration and feedback.
- Ensures the app remains in a deployable state at all times.


## Manual Review
This `README.md` file contains all the required sections for review as part of the Airbnb Clone Project setup.

GitHub Repository: [airbnb-clone-project](https://github.com/DyphineAnyanga/airbnb-clone-project)
