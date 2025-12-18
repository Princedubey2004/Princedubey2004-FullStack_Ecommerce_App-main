# E-Commerce Platform
A modern full-stack e-commerce application built with Django REST Framework and React. 

This is a complete e-commerce solution featuring user authentication, product management, shopping cart functionality, and secure payment processing with Stripe integration.

# Table of contents
- [About_this_App](#About_this_App)
- [App_Overview](#App_Overview)
  * [Products_List_Page](#Products_List_Page)
  * [Product_Details_Page](#Product_Details_Page)
  * [Product_Edit_Page](#Product_Edit_Page)
  * [Add_Product_Page](#Add_Product_Page)
  * [Checkout_Page](#Checkout_Page)
  * [Payment_Confirmation_Page](#Payment_Confirmation_Page)
  * [Payment_successfull_Page](#Payment_successfull_Page)
  * [Orders_Page_For_User](#Orders_Page_For_User)
  * [Orders_Page_For_Admin](#Orders_Page_For_Admin)
  * [Address_Settings_Page](#Address_Settings_Page)
  * [Address_Create_Page](#Address_Create_Page)
  * [Address_Edit_Page](#Address_Edit_Page)
  * [Card_Settings_Page](#Card_Settings_Page)
  * [Card_Update_Page](#Card_Update_Page)
  * [Login_Page](#Login_Page)
  * [Register_Page](#Register_Page)
  * [User_Account_Page](#User_Account_Page)
  * [Update_User_Account_Page](#Update_User_Account_Page)
  * [Delete_User_Account_Page](#Delete_User_Account_Page)
  * [Other_Functionalities](#Other_Functionalities)
- [Installation](#Installation)
  * [Backend](#backend)
  * [Frontend](#frontend)

## About This Application
A comprehensive e-commerce platform where users can browse products, create accounts, and make purchases using Stripe payment integration. 

**Key Features:**
- Browse products without authentication
- User registration and authentication with JWT tokens
- Secure payment processing with Stripe
- Shopping cart and order management
- Admin panel for product management
- User account management (update/delete)
- Address and payment card management
- Order tracking and history

**Security:**
- All user data is securely managed
- JWT token-based authentication
- Secure payment processing
- Account deletion removes all associated data (addresses, cards, orders) 

## App_Overview
### Features Overview

**Products**
- Products List Page: Browse all available products
- Product Details Page: View detailed product information with purchase options
- Product Management (Admin): Create, update, and delete products

**Shopping Experience**
- Checkout Page: Secure checkout with Stripe payment integration
- Payment Confirmation: Review order before finalizing payment
- Payment Success: Order confirmation and receipt

**User Management**
- Login/Register: User authentication system
- User Account Page: View account details and admin privileges
- Update Account: Modify username, email, and password
- Delete Account: Remove account and all associated data

**Order Management**
- User Orders: View personal order history
- Admin Orders: Manage all customer orders with search functionality
- Delivery Status: Track order delivery status (admin feature)

**Payment & Address**
- Stripe Card Management: Add, update, and delete payment cards
- Address Management: Create, edit, and manage delivery addresses

### Technical Features
- **Authentication**: JWT (JSON Web Tokens) for secure user authentication
- **Security**: Comprehensive security checks for card creation and payment processing
- **API Protection**: JWT token validation on all protected endpoints
- **Payment Processing**: Secure Stripe integration for payment handling
- **RESTful API**: Django REST Framework for backend API
- **State Management**: Redux for frontend state management

## Installation

Follow these steps to set up the project locally:

**Prerequisites:**
- Python 3.10 or higher
- Node.js and npm
- Stripe account (for payment processing)

**Note:** You'll need to configure your Stripe API keys in the Django settings before running the project.

### Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Create a virtual environment:
   ```bash
   python3 -m venv venv
   # On Windows: python -m venv venv
   ```

3. Activate the virtual environment:
   ```bash
   source venv/bin/activate
   # On Windows: venv\Scripts\activate
   ```

4. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

5. Run database migrations:
   ```bash
   python manage.py migrate
   ```

6. Configure Stripe keys in `settings.py` (set environment variables):
   ```python
   STRIPE_TEST_PUBLISHABLE_KEY=your_publishable_key
   STRIPE_TEST_SECRET_KEY=your_secret_key
   ```

7. Start the Django development server:
   ```bash
   python manage.py runserver
   ```

The backend will run on `http://127.0.0.1:8000`

### Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the React development server:
   ```bash
   export NODE_OPTIONS=--openssl-legacy-provider
   npm start
   ```

   **Note:** On Windows, use `set NODE_OPTIONS=--openssl-legacy-provider` before `npm start`

The frontend will run on `http://localhost:3000`

## Technology Stack

- **Backend**: Django 3.2.4, Django REST Framework, PostgreSQL/SQLite
- **Frontend**: React 17, Redux, React Router, Bootstrap
- **Authentication**: JWT (djangorestframework-simplejwt)
- **Payment**: Stripe API
- **State Management**: Redux with Redux Thunk

## License

This project is private and proprietary.


