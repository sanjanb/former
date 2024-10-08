
# 🥕 Farm to Table E-Commerce Platform

Farm to Table is an e-commerce platform that connects farmers directly with consumers. Farmers can list their products, and consumers can purchase items directly through the platform. The platform facilitates seamless product listing, ordering, and transactions, ensuring that fresh produce reaches consumers efficiently.

## 🌟 Features

- **Farmer Registration/Login**: Farmers can register and log in to manage their product listings.
- **Buyer Registration/Login**: Buyers can register and log in to browse and purchase products.
- **Product Listings**: Farmers can add, update, or delete product listings.
- **Order Management**: Buyers can place orders, view order history, and manage payments.
- **Transaction Management**: Farmers can track transactions for their sales.
- **Secure Authentication**: JWT-based authentication for secure user login.

---

## 🚀 Getting Started

Follow these steps to get the application running on your local machine.

### **Prerequisites**

- [Node.js](https://nodejs.org/) (version 14 or higher)
- [MongoDB](https://www.mongodb.com/) (for local development or a cloud instance like MongoDB Atlas)

### **Installing Dependencies**

1. Clone this repository:

   ```bash
   git clone https://github.com/your-username/farm-to-table.git
   cd farm-to-table/former-backend
   ```

2. Install the dependencies:

   ```bash
   npm install
   ```

### **Environment Variables**

Create a `.env` file in the root directory of the project and add the following environment variables:

```plaintext
MONGODB_URI=<your_mongodb_connection_string>
JWT_SECRET=<your_jwt_secret>
PORT=5000
```

- Replace `<your_mongodb_connection_string>` with your MongoDB connection string.
- Replace `<your_jwt_secret>` with a secure string to sign JWT tokens.

### **Running the Application**

To start the server, run:

```bash
node server.js
```

The server will start on `http://localhost:5000`. You should see the message "MongoDB connected" if the connection is successful.

---

## 📜 API Endpoints

Here are the available API endpoints:

### **Authentication**

- `POST /api/auth/register` – Register a new user (farmer or buyer)
- `POST /api/auth/login` – Log in a user (returns a JWT)

### **Products**

- `POST /api/products` – Add a new product (Farmer only)
- `GET /api/products` – Get all products
- `GET /api/products/:id` – Get a specific product by ID
- `PUT /api/products/:id` – Update a product (Farmer only)
- `DELETE /api/products/:id` – Delete a product (Farmer only)

### **Orders**

- `POST /api/orders` – Create a new order (Buyer only)
- `GET /api/orders/:buyerId` – Get all orders for a specific buyer

### **Transactions**

- `POST /api/transactions` – Record a transaction (Farmer only)
- `GET /api/transactions/:farmerId` – Get all transactions for a specific farmer

---

## ⚙️ Technologies Used

- **Back-end**: Node.js, Express, MongoDB, Mongoose
- **Authentication**: JWT (JSON Web Tokens)
- **Database**: MongoDB (Atlas for cloud, or local)
- **Middleware**: CORS, Body-Parser

---

## 🛠 Future Enhancements

- **Third-Party Logistics Integration**: To manage product delivery logistics.
- **Payment Gateway Integration**: To manage payments directly through the platform.
- **Notifications System**: To notify farmers and buyers about orders and transactions.

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the project.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a pull request.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
