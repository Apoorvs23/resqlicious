# ResQlicious: Restaurant Ordering and Surplus Food Platform

This project is a comprehensive restaurant ordering platform designed to connect restaurants and users while addressing the critical issue of food waste. ResQlicious empowers restaurants, supermarkets, and users to minimize food waste by facilitating the sale of surplus food and groceries at discounted rates. The platform comprises three main components:

1. **Backend** - Powers the application with APIs and handles business logic.  
   Repository: [Resqlicious Backend](https://github.com/Apoorvs23/resqlicious-backend)

2. **Frontend for Restaurant Owners** - Enables restaurants to manage profiles, menus, and orders.  
   Repository: [Resqlicious Frontend (Retailer)](https://github.com/Apoorvs23/resqlicious-frontend-retailer)

3. **Frontend for Users** - Allows users to browse restaurants, place orders, and manage accounts.  
   Repository: [Resqlicious Frontend (User)](https://github.com/Apoorvs23/resqlicious-frontend)

---

## Problem Statement

Food waste is a pressing global issue:

- **5.8 million people** in Canada face food insecurity.
- Restaurants and hotels generate **1.44 million tonnes** of surplus food annually.
- This leads to a staggering **\$7.14 billion** in avoidable food loss.

Surplus food waste contributes to environmental degradation, economic losses, and missed opportunities to feed those in need. ResQlicious provides a sustainable and efficient solution to these challenges.

---

## Solution

ResQlicious offers a platform where:

- Restaurants can sell surplus food at discounted prices.
- Supermarkets can list grocery items nearing their best-before date.
- Users can buy food and groceries at affordable rates while reducing waste.

This approach ensures surplus food is rerouted to those who require it, addressing food insecurity and environmental concerns.

---

## Features

### **Backend**

- Built with Spring Boot.
- Features include:
  - User registration, login, and JWT-based authentication.
  - Database migrations from H2 (local testing) to SQL for scalability.
  - Comprehensive order management:
    - Create and view orders.
    - Retrieve orders by user ID.
  - "Forget Password" feature for secure credential recovery.
  - Secure file uploads with random file name generation for images.
  - Stripe integration for payment processing.
  - CORS configuration for cross-origin access during development.

#### Example `application.properties` Configuration:

```properties
server.port=8082
spring.application.name=resqlicious-backend

# DB Config
spring.datasource.url=jdbc:mysql://localhost:3306/resqdb
spring.datasource.username=root
spring.datasource.password=pass
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQLDialect
spring.jpa.hibernate.ddl-auto=none
spring.jpa.show-sql=true

springdoc.override-with-generic-response=false

spring.jpa.properties.hibernate.format_sql=true
logging.level.org.hibernate.SQL=DEBUG
logging.level.org.hibernate.type.descriptor.sql.BasicBinder=TRACE

project.image=images/

# Maximum file size
spring.servlet.multipart.max-file-size=10MB
spring.servlet.multipart.max-request-size=10MB

# Spring Mail properties for Gmail
spring.mail.host=smtp.gmail.com
spring.mail.port=587
spring.mail.username=shamma@uwindsor.ca
spring.mail.password=xxx
spring.mail.properties.mail.smtp.auth=true
spring.mail.properties.mail.smtp.starttls.enable=true
spring.mail.properties.mail.smtp.starttls.required=true
```

### **Restaurant Frontend**

- Developed with React.
- Key Features:
  - Manage restaurant profiles, including image uploads.
  - Add, view, and edit menus with detailed information (e.g., dish description, quantity, and images).
  - Handle orders dynamically.
  - Optimized for performance and user experience.

### **User Frontend**

- Built with React.
- Key Features:
  - User authentication (register, login, logout, and reset password).
  - Browse restaurants and view detailed profiles.
  - Add dishes to a cart, place orders, and manage orders dynamically.
  - Search restaurants by name or cuisine.
  - Responsive design for enhanced usability.

### **Supermarket Functionality**

- Enables supermarkets to list surplus groceries.
- Real photos of items for transparency.
- Discounts for items nearing best-before dates.

### **Future Scope**

- Expand to events, office cafeterias, and educational institutions.

---

## Competitive Advantages

1. **No "Surprise Bags"** - Unlike competitors, users know exactly what they are buying.
2. **Transparent Pricing and Reviews** - Restaurants and supermarkets set their prices, and users see detailed reviews.
3. **Real Photos** - Actual images of surplus food and groceries, avoiding discrepancies.
4. **Broader Reach** - Supports local grocery stores and independent businesses.
5. **All-in-One Solution** - Combines surplus food from restaurants and supermarkets into a single platform.

---

## Installation and Setup

### **Prerequisites**

- Java 11 or higher.
- Node.js and npm.
- A SQL-compatible database (e.g., MySQL, PostgreSQL).
- Stripe account for payment processing.

### **Backend Setup**

1. Clone the backend repository:

   ```bash
   git clone https://github.com/Apoorvs23/resqlicious-backend
   cd resqlicious-backend
   ```

2. Configure the database in `application.properties`:

   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/resqlicious
   spring.datasource.username=<username>
   spring.datasource.password=<password>
   stripe.api.key=<your-stripe-api-key>
   ```

3. Run the application:

   ```bash
   ./mvnw spring-boot:run
   ```

### **Frontend Setup**

#### Restaurant Frontend

1. Clone the restaurant frontend repository:

   ```bash
   git clone https://github.com/Apoorvs23/resqlicious-frontend-retailer
   cd resqlicious-frontend-retailer
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Start the development server:

   ```bash
   npm start
   ```

#### User Frontend

1. Clone the user frontend repository:

   ```bash
   git clone https://github.com/Apoorvs23/resqlicious-frontend
   cd resqlicious-frontend
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Start the development server:

   ```bash
   npm start
   ```

---

## Contribution Guidelines

1. Fork the repository and create a new branch for your feature or bug fix.
2. Ensure your code adheres to coding standards.
3. Run tests locally before submitting a pull request.
4. Submit a pull request with a clear description of your changes.

---

## Sustainability Impact

- Reduces food waste and its associated environmental footprint.
- Supports community well-being by making affordable food available.
- Helps businesses recover costs from surplus food.

---

## Acknowledgments

- Developed using Spring Boot and React.
- Stripe API for payment integration.
- Data and market insights derived from user and restaurant feedback.

---

## License

This project is licensed under the [MIT License](LICENSE).

---

Feel free to share feedback or suggestions for further improvement!

