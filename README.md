# 💊 Medic Panda – Online Pharmacy E-Commerce Backend

Medic Panda is a modern and scalable backend API for a single-vendor online pharmacy e-commerce application. It enables customers to browse healthcare products, manage their carts, place orders, make secure payments, and manage their accounts.

Built with **TypeScript, Node.js, Express.js, MongoDB, Mongoose, Zod, and JWT**, this backend provides secure authentication, product management, order processing, payment integration, and role-based access control.

## 🔗 Important Links

- **Live Demo:** [Medic Panda](https://medic-panda.vercel.app/)
- **Frontend Repository:** [Medic Panda Frontend](https://github.com/Sujoy-Kumar-Das/medic-panda-frontend)
- **Backend Repository:** [Medic Panda Backend](https://github.com/Mesbah-AI/medic-panda-backend)

## 🚀 Key Features

### 🔐 Authentication & Authorization

- User registration and login
- JWT-based access and refresh tokens with cookie support
- Email verification using OTP
- Password reset functionality
- Secure password hashing with bcrypt
- Role-based access control for Admin, Super Admin, and Customer

### 🛍️ Product Management

- Create, update, delete, and retrieve products
- Product categorization and manufacturer management
- Stock and inventory management
- Product discounts and time-based discount status handling
- Product reviews and detailed product information

### 🛒 Cart & Order Management

- Add, update, and remove cart items
- Order placement and order history
- Inventory validation during order processing
- Secure order processing and payment workflow
- Admin-managed order status updates

### ⭐ Reviews & Replies

- Authenticated customer reviews
- Review reply functionality
- Structured review management for future moderation enhancements

### 💳 Payment Integration

- Integrated with the SSLCommerz payment gateway
- Secure payment initiation and transaction handling
- Sandbox and live payment configuration support
- Payment success, failure, and cancellation callbacks
- Order status updates based on payment results

### 📧 Email & OTP Services

- Email verification
- OTP-based password recovery
- Configurable email templates and verification redirects

### 🛡️ Validation & Error Handling

- Request validation using Zod
- Centralized error handling middleware
- Consistent API error responses
- Environment-based application configuration

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| TypeScript | Type safety and maintainable code |
| Node.js | JavaScript runtime |
| Express.js | Backend API framework |
| MongoDB | NoSQL database |
| Mongoose | MongoDB object modeling |
| Zod | Data validation |
| JWT | Authentication and authorization |
| bcrypt | Password hashing |
| dotenv | Environment variable management |
| SSLCommerz | Online payment processing |

## 📁 Project Structure

```text
src/
├── app/
├── builder/
├── config/
├── DB/
├── emailTemplate/
├── errors/
├── helpers/
├── interface/
├── modules/
│   ├── admin/
│   ├── auth/
│   ├── blog/
│   ├── cart/
│   ├── category/
│   ├── customer/
│   ├── manufacturer/
│   ├── meta/
│   ├── orders/
│   ├── payment/
│   ├── productDetails/
│   ├── product/
│   ├── review-reply/
│   ├── reviews/
│   ├── user/
│   └── wishList/
├── middlewares/
├── routes/
├── ssl/
├── utils/
├── app.ts
└── server.ts
```

## ⚙️ Setup & Installation

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/)
- [Git](https://git-scm.com/)
- MongoDB database (local or cloud)

### 1. Clone the Repository

```bash
git clone https://github.com/Mesbah-AI/medic-panda-backend.git
cd medic-panda-backend
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Environment Variables

Create a `.env` file in the project root and add the following configuration:

```env
PORT=5000
db_url=YOUR_MONGODB_URL
saltRounds=10

# JWT & OTP Secrets
jwt_access_token=YOUR_ACCESS_SECRET
jwt_refresh_token=YOUR_REFRESH_SECRET
otp_token=YOUR_OTP_SECRET

# OTP Verification
otp_verification_url=
node_env=development

# SSLCommerz Configuration
SSL_URL=https://sandbox.sslcommerz.com/gwprocess/v4/api.php
SSL_StoreID=YOUR_STORE_ID
SSL_PASSWORD=YOUR_STORE_PASSWORD

# Payment Callback URLs
ssl_success_url=https://your-backend.com/api/v1/success-payment
ssl_failed_url=https://your-backend.com/api/v1/failed-payment
ssl_cancel_url=https://your-backend.com/api/v1/success-cancel

# Frontend URLs
success_frontend_link=https://your-frontend.com/success-payment
failed_frontend_link=https://your-frontend.com/failed-payment
verify_email_frontend_link=https://your-frontend.com/verify-email
forgot_password_frontend_link=https://your-frontend.com/reset-password
email_verification_redirect_link=https://your-frontend.com/dashboard/security
base_frontend_link=https://your-frontend.com/

# Authentication Email
auth_user_email=your@email.com
auth_user_password=YOUR_APP_PASSWORD

# Token Expiry
jwt_access_token_validation=5m
jwt_refresh_token_validation=30d

# Super Admin Setup
supper_admin_email=admin@email.com
supper_admin_password=CHANGE_THIS_PASSWORD
```

**Important:** Replace all placeholder values with your actual credentials and URLs. Never commit your `.env` file or expose secrets in a public repository.

### 4. Start the Development Server

```bash
npm run dev
```

The backend will run at:

```text
http://localhost:5000
```

Make sure MongoDB and the required environment variables are configured before starting the application.

## 🔒 Security Notes

- Store credentials and secret keys in environment variables.
- Use strong, unique JWT and OTP secrets.
- Keep production payment credentials private.
- Configure HTTPS and secure cookie settings for production.
- Use the SSLCommerz sandbox for testing before switching to live mode.

## 🙋‍♂️ Author

**Mesbah**

- **GitHub:** [@Mesbah-AI](https://github.com/Mesbah-AI)
- **Backend Repository:** [medic-panda-backend](https://github.com/Mesbah-AI/medic-panda-backend)

---

If you find this project useful, consider giving the repository a ⭐ on GitHub.

