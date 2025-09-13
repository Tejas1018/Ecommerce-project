# E-Commerce Application - Microservices Architecture

A modern E-Commerce application built using Spring Boot microservices architecture. This project demonstrates the implementation of a scalable, maintainable, and distributed E-Commerce system.

## Microservices Overview

The application consists of the following microservices:

### 1. Product Service
- Manages product catalog and inventory
- Handles product categories and classifications
- Features:
  - CRUD operations for products
  - Category management
  - Product search and filtering
  - Integration with external product services (FakeStore API)
- Key Components:
  - Product Controller: REST endpoints for product operations
  - Category Management
  - Custom Exception Handling
  - Multiple Database Inheritance Strategies
  - Projections for optimized queries

### 2. Payment Service
- Handles all payment-related operations
- Supports multiple payment gateways
- Features:
  - Integration with Razorpay and Stripe
  - Secure payment processing
  - Payment status tracking
- Key Components:
  - Payment Gateway Interface
  - Implementation for multiple payment providers
  - Payment status management
  - Secure transaction handling

### 3. User Service
- Manages user accounts and authentication
- Handles user profiles and preferences
- Features:
  - User registration and authentication
  - Profile management
  - User authorization
  - Session management

## Technical Stack

- **Framework**: Spring Boot
- **Language**: Java
- **Build Tool**: Maven
- **Database**: MySql
- **API Documentation**: Postman
- **Version Control**: Git

## Getting Started

### Prerequisites
- Java JDK 11 or higher
- Maven
- Git
- Your preferred IDE (IntelliJ IDEA recommended)

### Installation and Setup

1. Clone the repository:
```bash
git clone https://github.com/Tejas1018/Ecommerce-project.git
```

2. Navigate to each service directory and build:
```bash
cd ProductService
mvn clean install

cd ../PaymentService
mvn clean install

cd ../UserService
mvn clean install
```

3. Start each service:
```bash
# Start Product Service
cd ProductService
mvn spring-boot:run

# Start Payment Service
cd ../PaymentService
mvn spring-boot:run

# Start User Service
cd ../UserService
mvn spring-boot:run
```

## Service Endpoints

### Product Service
- Base URL: `http://localhost:[port]/api/products`
- Endpoints:
  - GET `/products` - Get all products
  - GET `/products/{id}` - Get product by ID
  - POST `/products` - Create new product
  - PUT `/products/{id}` - Update product
  - DELETE `/products/{id}` - Delete product
  - GET `/categories` - Get all categories

### Payment Service
- Base URL: `http://localhost:[port]/api/payments`
- Endpoints:
  - POST `/process` - Process payment
  - GET `/status/{id}` - Get payment status
  - POST `/refund` - Process refund

### User Service
- Base URL: `http://localhost:[port]/api/users`
- Endpoints:
  - POST `/register` - Register new user
  - POST `/login` - User login
  - GET `/profile` - Get user profile
  - PUT `/profile` - Update user profile

## Architecture

The application follows a microservices architecture with:
- Independent deployment capability
- Service isolation
- Database per service
- REST communication between services
- Scalable components

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Spring Boot Documentation
- Microservices Design Patterns
- Payment Gateway Providers (Razorpay, Stripe)

## Contact

Your Name - [Your Email]
Project Link: https://github.com/Tejas1018/Ecommerce-project
