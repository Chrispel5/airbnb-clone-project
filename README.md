# airbnb-clone-project

# Airbnb Clone Project

## Overview
This project is a simplified clone of the Airbnb platform. It aims to replicate the core functionalities of property rental—such as listing, booking, reviewing, and managing stays—using modern web development technologies.

### Project Goals
- Build a scalable and secure web application.
- Learn full-stack development practices.
- Apply CI/CD and DevOps tools.

---

## Team Roles

- **Backend Developer**: Implements business logic and REST/GraphQL APIs.
- **Frontend Developer**: Designs user interface and connects frontend to backend.
- **Database Administrator (DBA)**: Designs, manages, and optimizes database schema.
- **DevOps Engineer**: Sets up CI/CD pipelines, containerization, and deployment.
- **Project Manager**: Oversees task delegation, timelines, and team coordination.

---

## Technology Stack

- **Django**: Web framework to handle backend logic and APIs.
- **PostgreSQL**: Relational database to store users, properties, bookings, etc.
- **GraphQL**: Query language for fetching frontend data flexibly.
- **Docker**: Containerizes the application for consistent environments.
- **GitHub Actions**: Automates testing and deployment workflows.
- **React** (optional): For building a dynamic frontend interface.

---

## Database Design

### Entities and Fields

- **Users**
  - `id`, `name`, `email`, `password_hash`
- **Properties**
  - `id`, `owner_id`, `title`, `location`, `price`
- **Bookings**
  - `id`, `user_id`, `property_id`, `start_date`, `end_date`
- **Reviews**
  - `id`, `user_id`, `property_id`, `rating`, `comment`
- **Payments**
  - `id`, `booking_id`, `amount`, `status`

### Relationships

- A **User** can have many **Properties**
- A **Booking** belongs to one **User** and one **Property**
- A **Review** is written by a **User** for a **Property**
- A **Payment** is made for a **Booking**

---

## Feature Breakdown

- **User Management**: Handles registration, login, profile updates, and role-based access.
- **Property Management**: Allows users to list, update, and delete rental properties.
- **Booking System**: Users can book available properties with automated date checks.
- **Review System**: Allows guests to leave reviews and ratings for hosts.
- **Payment Integration**: Secure handling of payments for bookings using Stripe or PayPal.

---

## API Security

- **Authentication**: Users must log in with JWT tokens or session-based auth.
- **Authorization**: Ensures only owners can modify their own property listings.
- **Rate Limiting**: Prevents abuse by limiting API calls per user/IP.
- **Input Validation**: Sanitizes and validates all API inputs to avoid injection attacks.

### Why It Matters
- Protects sensitive user data and payments.
- Prevents unauthorized access or manipulation of data.
- Ensures overall application stability and trustworthiness.

---

## CI/CD Pipeline

- **CI/CD (Continuous Integration/Continuous Deployment)** automates testing and deployment to improve reliability and development speed.
- **Tools Used**:
  - **GitHub Actions**: Automates testing and deployment processes on each push.
  - **Docker**: Packages the app in containers for consistent environments.
  - **Heroku/AWS/GCP** (optional): Platform for deploying the final product.

---


