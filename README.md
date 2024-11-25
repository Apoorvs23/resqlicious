# Restaurant Ordering Platform

This project is a complete restaurant ordering platform that connects restaurants with users. The platform is composed of three main components:  
1. **Backend** - Powers the application with APIs and handles business logic.  
   Repository: [Resqlicious Backend](https://github.com/Apoorvs23/resqlicious-backend)  
2. **Frontend for Restaurant Owners** - Enables restaurants to manage their profiles, menus, and orders.  
   Repository: [Resqlicious Frontend (Retailer)](https://github.com/Apoorvs23/resqlicious-frontend-retailer)  
3. **Frontend for Users** - Allows users to browse restaurants, place orders, and manage their accounts.  
   Repository: [Resqlicious Frontend (User)](https://github.com/Apoorvs23/resqlicious-frontend)  

---

## Features

### **Backend**
- Built with Spring Boot.
- Supports user registration, login, and JWT-based authentication.
- Database migrations from H2 (local testing) to SQL for scalability.
- Comprehensive order management:
  - Create and view orders.
  - Retrieve orders by user ID.
- "Forget Password" feature for secure credential recovery.
- Secure file uploads with random file name generation for images.
- Stripe integration for payment processing.
- CORS configuration for cross-origin access during development.

### **Restaurant Frontend**
- Developed with React.
- Key Features:
  - Manage restaurant profiles, including image uploads.
  - Add, view, and edit menus with detailed information (e.g., dish description, quantity, and images).
  - Handle orders dynamically.
- Seamless user experience with robust bug fixes and performance optimizations.

### **User Frontend**
- Built with React.
- Key Features:
  - User authentication (register, login, logout, and reset password).
  - Browse restaurants and view detailed profiles.
  - Add dishes to a cart, place orders, and manage orders dynamically.
  - Search restaurants by name or cuisine.
  - Responsive design for better usability.

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
2. Configure the database in `application.properties`.
3. Run the application:
   ```bash
   ./mvnw spring-boot:run
   ```

### **Restaurant Frontend Setup**
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

### **User Frontend Setup**
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
2. Ensure that your code adheres to the coding standards outlined in the project.
3. Submit a pull request with a clear description of your changes.

---

## Acknowledgments
- Developed with Spring Boot and React.
- Stripe API used for payment integration.
- Thanks to all contributors for their efforts in making this project successful.

---

## License
This project is licensed under the [MIT License](LICENSE).

---

Feel free to share feedback or suggestions for further improvement!
