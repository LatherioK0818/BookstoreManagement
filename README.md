# Bookstore Management System

## 📌 Project Overview

The **Bookstore Management System** is a full-stack application designed to automate and streamline the operations of a bookstore. The system replaces traditional manual processes with a **fully automated** digital solution that manages inventory, tracks sales, and facilitates seamless order processing.

## 🚀 Features

- **User Authentication** (Customers, Employees, and Admins)
- **Inventory Management** (Adding, Updating, and Removing Books)
- **Sales Records Management**
- **Customer Orders** (Online & In-Store)
- **Supplier Orders**
- **Real-time Inventory Updates**
- **Integration with Payment Gateways**

## 📂 Project Structure

The project follows a **three-tier architecture**:
1. **Frontend** - Built with React.js for a responsive and user-friendly interface.
2. **Backend** - Developed using Node.js with Express.js.
3. **Database** - PostgreSQL with Sequelize ORM for managing data.

---

## 🛠️ Tech Stack

### **Frontend:**

- React.js
- React Router
- Axios
- Bootstrap

### **Backend:**

- Node.js with Express.js
- Sequelize ORM
- JSON Web Tokens (JWT) for authentication

### **Database:**

- PostgreSQL

### **Tools:**

- GitHub for version control
- WSL (if using Windows)
- Postman for API testing
- Docker (optional for containerization)

---

## 📖 Setup & Installation

### **1️⃣ Check Your CLI Environment**

Before running any command, check your CLI type:
```sh
echo "CLI Type: $(uname -a)"
```
If using **WSL**, check the Windows version:
```sh
wsl --list --verbose
```

### **2️⃣ Clone the Repository**

```sh
git clone https://github.com/YOUR_USERNAME/bookstore-management.git
cd bookstore-management
```

### **3️⃣ Backend Setup**

```sh
cd backend
npm install
```

#### **Create `.env` File**

```sh
touch .env
```
Add the following environment variables:
```sh
DATABASE_URL=postgres://USER:PASSWORD@localhost:5432/bookstore
JWT_SECRET=your_secret_key
PORT=5000
```

#### **Initialize Sequelize Configuration**

```sh
npx sequelize-cli init
```
Manually edit `backend/config/config.json`:
```json
{
  "development": {
    "username": "your_db_username",
    "password": "your_db_password",
    "database": "bookstore",
    "host": "127.0.0.1",
    "dialect": "postgres"
  }
}
```

#### **Run Migrations**

```sh
npx sequelize-cli db:migrate
```

#### **Start the Backend Server**

```sh
nodemon backend/server.js
```

### **4️⃣ Frontend Setup**

```sh
cd ../frontend
npx create-react-app frontend
cd frontend
npm install
```

#### **Start React App**

```sh
npm start
```

---

## 📝 API Endpoints

### **Authentication**

| Method | Endpoint         | Description             |
|--------|-----------------|-------------------------|
| POST   | `/signup`       | Register a new user    |
| POST   | `/login`        | Authenticate user      |

### **Books**

| Method | Endpoint         | Description               |
|--------|-----------------|---------------------------|
| GET    | `/books`        | Get all books             |
| POST   | `/books`        | Add a new book (Admin)    |

### **Orders**

| Method | Endpoint         | Description             |
|--------|-----------------|-------------------------|
| POST   | `/orders`       | Create a new order      |
| GET    | `/orders`       | Get all orders          |

---

## 🎯 Contribution Guidelines

1. **Fork the repository**.
2. Create a **feature branch**.
3. Commit your changes.
4. Open a **pull request**.

---

## 🔥 Future Enhancements

- Add **user roles and permissions**.
- Implement **real-time notifications**.
- Integrate **third-party payment gateways**.
- Develop a **mobile-friendly UI**.

---

## 🏆 Author & Acknowledgments

Developed by **Latherio Kidd** as part of a project to enhance **bookstore automation**.

---

## 📜 License

This project is **open-source** and available under the MIT License.

---

## ⭐ Support

If you like this project, consider **starring** the repo!

🚀 Happy Coding!

