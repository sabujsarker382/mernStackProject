# mernStackProject

## Overview
This is the backend API for an e-commerce application, built using **Express.js** and **MongoDB**. It provides authentication, product management, category management, and order handling functionalities.

## Features
✅ User Authentication (Signup, Login, OTP, Password Reset)  
✅ Admin Role Management  
✅ Product Management (CRUD operations)  
✅ Category Management  
✅ Order Management  
✅ Secure API Endpoints  
✅ Search & Filtering  
✅ Image Uploading using `express-formidable`

## Tech Stack
- **Node.js** (Backend Runtime)
- **Express.js** (Web Framework)
- **MongoDB & Mongoose** (Database & ORM)
- **JWT (JSON Web Token)** (Authentication)
- **Bcrypt.js** (Password Hashing)
- **Express Formidable** (File Handling)

## Installation & Setup

### Prerequisites
Ensure you have the following installed:
- **Node.js** (Latest LTS version)
- **MongoDB** (Local or Cloud-based like MongoDB Atlas)

### Steps to Install
1. Clone the repository:
   ```sh
   git clone https://github.com/sabujsarker382/mernStackProject.git
   cd mernStackProject
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Set up environment variables:
   - Create a `.env` file in the root directory.
   - Add the following environment variables:
     ```sh
     MONGO_URI=your_mongodb_connection_string
     JWT_SECRET=your_secret_key
     ```
4. Start the server:
   ```sh
   npm start
   ```
   The API will run at `http://localhost:5000` (default port).

## API Endpoints

### **Authentication Routes** (`/api/auth`)
| Method | Endpoint      | Description |
|--------|-------------|-------------|
| POST   | `/register` | User registration |
| POST   | `/login`    | User login |
| GET    | `/auth-check` | Check if user is authenticated |
| GET    | `/admin-check` | Check if user is an admin |
| PUT    | `/profile`  | Update user profile |

### **Category Routes** (`/api/category`)
| Method | Endpoint | Description |
|--------|---------|-------------|
| POST   | `/category` | Create a new category (Admin) |
| PUT    | `/category/:categoryId` | Update a category (Admin) |
| DELETE | `/category/:categoryId` | Delete a category (Admin) |
| GET    | `/categories` | Get all categories |
| GET    | `/category/:slug` | Get a category by slug |
| GET    | `/products-by-category/:slug` | Get products in a category |

### **Product Routes** (`/api/product`)
| Method | Endpoint | Description |
|--------|---------|-------------|
| POST   | `/product` | Create a product (Admin) |
| GET    | `/products` | Get all products |
| GET    | `/product/:slug` | Get product details |
| GET    | `/product/photo/:productId` | Get product image |
| DELETE | `/product/:productId` | Delete a product (Admin) |
| PUT    | `/product/:productId` | Update a product (Admin) |
| POST   | `/filtered-products` | Get filtered products |
| GET    | `/products-count` | Get total product count |
| GET    | `/list-products/:page` | Paginated product listing |
| GET    | `/products/search/:keyword` | Search products by keyword |
| GET    | `/related-products/:productId/:categoryId` | Get related products |

### **Order Routes** (`/api/orders`)
| Method | Endpoint | Description |
|--------|---------|-------------|
| GET    | `/orders` | Get user orders |
| GET    | `/all-orders` | Get all orders (Admin) |

## Deployment
For deployment, use:
- **Vercel** or **Render** for Node.js hosting
- **MongoDB Atlas** for database hosting
- **Cloudinary** or **Firebase Storage** for image hosting

## Contribution
If you'd like to contribute:
1. Fork the repository
2. Create a new feature branch (`git checkout -b feature-name`)
3. Commit your changes (`git commit -m "Add new feature"`)
4. Push to your branch (`git push origin feature-name`)
5. Create a Pull Request




