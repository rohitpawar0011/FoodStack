# 🍔 Food-App - Full-Stack Food Ordering & Delivery Platform

A modern, full-stack food ordering and delivery web application that provides a seamless experience for customers to explore restaurants, manage their cart, and place real-time orders with ease. The system features a comprehensive admin panel for restaurant management, menu updates, order tracking, and user management.

[![Deployment](https://img.shields.io/badge/Frontend-Render-46E3B7?style=flat&logo=render)](https://food-app-frontend-3vxz.onrender.com)
[![Node.js](https://img.shields.io/badge/Node.js-20.15.0-339933?style=flat&logo=node.js)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-18.2.0-61DAFB?style=flat&logo=react)](https://reactjs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Database-47A248?style=flat&logo=mongodb)](https://www.mongodb.com/)

## 🧠 Project Overview

Food-App is a comprehensive food ordering and delivery platform that bridges customers with restaurants through an intuitive web interface. It supports the complete food ordering lifecycle from browsing menus to real-time order tracking and delivery.

**Live Demo:** [food-app-frontend-3vxz.onrender.com](https://food-app-frontend-3vxz.onrender.com)

## 🚀 Key Features

### 🍔 User-Friendly Food Ordering
- **Browse Menu**: Users can explore a wide variety of dishes from different restaurants
- **Dynamic Cart Management**: Add multiple items to cart, update quantities, and view total cost in real-time
- **Smooth Checkout**: Streamlined checkout process with order summary and delivery details
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices

### 🧾 Secure Authentication & User Management
- **JWT-Based Authentication**: Secure login and signup using JSON Web Tokens
- **Role-Based Access Control**: Separate user and admin roles for better security
- **User Profiles**: Maintain user information, order history, and delivery addresses
- **Password Encryption**: Secure password storage using bcrypt

### 📦 Real-Time Order Tracking
- **Live Order Status**: Track orders from placement to delivery in real-time
- **Order Stages**: 
  - 📝 Pending
  - 👨‍🍳 Preparing
  - 🚚 Out for Delivery
  - ✅ Delivered
- **Order History**: View past orders and their details
- **Status Notifications**: Get updates as order status changes

### 💳 Online Payment Integration
- **Secure Payment Gateway**: Integrated Stripe for safe online transactions
- **Encrypted Payment Flow**: All payment data is encrypted and secure
- **Multiple Payment Methods**: Support for various payment options
- **Order Verification**: Automatic order confirmation after successful payment

### 🧑‍💼 Admin Panel
- **Menu Management**: Add, update, or remove food items from the menu
- **Availability Control**: Manage food item availability in real-time
- **Order Management**: View all orders and update their status
- **Sales Analytics**: Track daily sales and order performance
- **User Management**: View registered users and their order history

## 🧩 System Architecture

### 🖥️ Frontend (React.js + Vite)
- **Framework**: React 18.2.0 with modern hooks
- **Build Tool**: Vite for fast development and optimized builds
- **Routing**: React Router DOM for seamless navigation
- **State Management**: React Context API and hooks
- **HTTP Client**: Axios for API communication
- **Notifications**: React Toastify for user feedback
- **Styling**: Modern CSS with responsive design

### ⚙️ Backend (Node.js + Express.js)
- **Runtime**: Node.js 20.15.0
- **Framework**: Express.js for RESTful API
- **Authentication**: JWT (JSON Web Tokens)
- **Password Hashing**: bcrypt.js for secure password storage
- **File Upload**: Multer for handling food item images
- **Payment**: Stripe integration for online payments
- **Validation**: Validator.js for input validation
- **CORS**: Enabled for cross-origin requests

### 🗄️ Database (MongoDB)
- **Database**: MongoDB with Mongoose ODM
- **Collections**:
  - Users
  - Food Items
  - Orders
  - Cart Items
- **Schema Validation**: Mongoose schemas for data integrity

## 📁 Project Structure

```
Food-App/
├── frontend/                 # Customer-facing React application
│   ├── src/
│   │   ├── components/      # Reusable React components
│   │   ├── pages/           # Page components
│   │   ├── context/         # React Context for state management
│   │   ├── assets/          # Images and static files
│   │   └── App.jsx          # Main application component
│   ├── public/              # Public static files
│   └── package.json         # Frontend dependencies
│
├── admin/                    # Admin panel React application
│   ├── src/
│   │   ├── components/      # Admin-specific components
│   │   ├── pages/           # Admin page components
│   │   ├── assets/          # Admin assets
│   │   └── App.jsx          # Admin application component
│   └── package.json         # Admin dependencies
│
└── backend/                  # Node.js Express server
    ├── config/              # Configuration files
    ├── controllers/         # Request handlers
    ├── middlewares/         # Custom middleware (auth, etc.)
    ├── models/              # Mongoose schemas
    ├── routes/              # API route definitions
    │   ├── userRoute.js     # User authentication routes
    │   ├── foodRoute.js     # Food item routes
    │   ├── cartRoute.js     # Shopping cart routes
    │   └── orderRoute.js    # Order management routes
    ├── uploads/             # Uploaded food images
    ├── server.js            # Main server file
    └── package.json         # Backend dependencies
```

## 🛠️ Tech Stack

### Frontend
- **React** 18.2.0 - UI library
- **Vite** 5.1.6 - Build tool
- **React Router DOM** 6.28.1 - Routing
- **Axios** 1.6.8 - HTTP client
- **React Toastify** 11.0.3 - Notifications
- **ESLint** - Code linting

### Admin Panel
- **React** 18.2.0
- **Vite** 5.2.0
- **React Router DOM** 6.28.2
- **Axios** 1.6.8
- **React Toastify** 10.0.5

### Backend
- **Node.js** 20.15.0
- **Express.js** 4.19.2 - Web framework
- **MongoDB** with Mongoose 8.3.2 - Database
- **JWT** 9.0.2 - Authentication
- **bcryptjs** 2.4.3 - Password hashing
- **Stripe** 15.3.0 - Payment processing
- **Multer** 1.4.5 - File uploads
- **Validator** 13.11.0 - Input validation
- **CORS** 2.8.5 - Cross-origin support
- **dotenv** 16.4.7 - Environment variables

## 🚀 Getting Started

### Prerequisites
- Node.js 20.15.0 or higher
- MongoDB database
- Stripe account for payment processing

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/SagarKharat94440/Food-App.git
   cd Food-App
   ```

2. **Setup Backend**
   ```bash
   cd backend
   npm install
   ```
   
   Create a `.env` file in the backend directory:
   ```env
   PORT=4000
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   STRIPE_SECRET_KEY=your_stripe_secret_key
   ```
   
   Start the backend server:
   ```bash
   npm run server
   ```

3. **Setup Frontend**
   ```bash
   cd ../frontend
   npm install
   ```
   
   Create a `.env` file in the frontend directory (if needed):
   ```env
   VITE_API_URL=http://localhost:4000
   ```
   
   Start the frontend development server:
   ```bash
   npm run dev
   ```

4. **Setup Admin Panel**
   ```bash
   cd ../admin
   npm install
   ```
   
   Start the admin panel:
   ```bash
   npm run dev
   ```

### Running the Application

- **Frontend**: http://localhost:5173 (default Vite port)
- **Admin Panel**: http://localhost:5174 (or next available port)
- **Backend API**: http://localhost:4000

## 📡 API Endpoints

### Authentication
- `POST /api/user/register` - Register new user
- `POST /api/user/login` - User login

### Food Items
- `GET /api/food/list` - Get all food items
- `POST /api/food/add` - Add new food item (Admin)
- `DELETE /api/food/remove` - Remove food item (Admin)

### Cart
- `POST /api/cart/add` - Add item to cart
- `POST /api/cart/remove` - Remove item from cart
- `GET /api/cart/get` - Get user's cart

### Orders
- `POST /api/order/place` - Place new order
- `GET /api/order/userorders` - Get user's orders
- `GET /api/order/list` - Get all orders (Admin)
- `POST /api/order/status` - Update order status (Admin)

## 🌐 Deployment

### Frontend Deployment (Render)
The frontend is hosted on Render at: **[food-app-frontend-3vxz.onrender.com](https://food-app-frontend-3vxz.onrender.com)**

**Deployment Steps:**
1. Connect your GitHub repository to Render
2. Select the frontend directory
3. Set build command: `npm install && npm run build`
4. Set publish directory: `dist`
5. Add environment variables if needed

### Backend Deployment
The backend can be deployed on platforms like:
- Render
- Heroku
- Railway
- AWS
- DigitalOcean

**Environment Variables Required:**
- `MONGODB_URI`
- `JWT_SECRET`
- `STRIPE_SECRET_KEY`
- `PORT`

## 🔒 Security Features

- **JWT Authentication**: Secure token-based authentication
- **Password Hashing**: Bcrypt encryption for password storage
- **Input Validation**: Server-side validation for all inputs
- **CORS Configuration**: Controlled cross-origin access
- **Environment Variables**: Sensitive data stored securely
- **Payment Security**: Stripe's PCI-compliant payment processing

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👨‍💻 Author

**Sagar Kharat**
- GitHub: [@SagarKharat94440](https://github.com/SagarKharat94440)

## 🙏 Acknowledgments

- React.js community for excellent documentation
- Express.js for the robust backend framework
- MongoDB for flexible database solution
- Stripe for secure payment processing
- All contributors and supporters of this project

## 📞 Support

For support, please open an issue in the repository.

---

⭐ **Star this repository if you found it helpful!**
