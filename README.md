# Bookstore Management System

## 📌 Project Overview

The **Bookstore Management System** is a **FastAPI-based backend** that allows users to:

- 📚 **Manage books** (add, view inventory)
- 🛒 **Purchase books** (process transactions)
- 🔐 **User authentication** (register, login with JWT security)
- 🛡 **Secure API endpoints** (role-based access control)

This API is designed to integrate with a **React frontend** (to be developed) and can be deployed using **Docker, AWS, or Heroku**.

---

## 🚀 Features

✅ **User Authentication** (Register/Login with JWT tokens)  
✅ **Book Inventory Management** (CRUD operations)  
✅ **Secure Transactions** (Purchase books, update stock)  
✅ **Database Integration** (PostgreSQL/SQLite with SQLAlchemy)  
✅ **FastAPI Docs** (Swagger UI at `/docs`)  
✅ **Unit Testing Support** (pytest)  

---

## 📂 Folder Structure

```plaintext

bookstore-management/
│── main.py                  # Root entry point for FastAPI app
│── requirements.txt          # List of dependencies
│── .env                      # Environment variables (database credentials, secret keys)
│── README.md                 # Project documentation
│
├── app/                      # Main application folder
│   ├── __init__.py
│   ├── main.py               # FastAPI setup & routes inclusion
│   ├── database.py           # Database connection (SQLAlchemy)
│   ├── models.py             # Database models (User, Book, Transaction)
│   ├── schemas.py            # Pydantic schemas for validation
│   ├── security.py           # Authentication & JWT token functions
│   ├── routes/               # API route handlers
│   │   ├── users.py          # User authentication (register, login)
│   │   ├── books.py          # Book inventory management
│   │   ├── transactions.py   # Purchase processing
│   ├── tests/                # Unit & integration tests
│   │   ├── test_users.py     # Tests for user authentication
│   │   ├── test_books.py     # Tests for book management
│   │   ├── test_sales.py     # Tests for transactions
│
├── frontend/                 # (Optional) React frontend (to be developed)
```

---

## 🛠 Installation & Setup

### 1️⃣ **Clone the Repository**

```bash
git clone https://github.com/yourusername/bookstore-management.git
cd bookstore-management
```

### 2️⃣ **Create a Virtual Environment**

```bash
python -m venv venv
source venv/bin/activate  # For Mac/Linux
venv\Scripts\activate     # For Windows
```

### 3️⃣ **Install Dependencies**

```bash
pip install -r requirements.txt
```

### 4️⃣ **Run the FastAPI Server**

```bash
python main.py
```

OR

```bash
uvicorn app.main:app --reload
```

### 5️⃣ **Test API Endpoints in Swagger UI**

Open in browser:  
📌 **<http://127.0.0.1:8000/docs>**  *(Swagger UI)*  
📌 **<http://127.0.0.1:8000/redoc>** *(Redoc UI)*

---

## 🛠 Environment Variables (`.env` file)

Create a `.env` file in the project root and configure:

```env
SECRET_KEY=your_secret_key_here
DATABASE_URL=sqlite:///./bookstore.db  # Change to PostgreSQL if needed
```

---

## 🛠 Running Tests

Run **pytest** to execute unit tests:

```bash
pytest
```

---

## 📌 Future Improvements

✅ **React Frontend** (Bookstore UI for browsing and purchasing)  
✅ **Admin Panel** (For book & order management)  
✅ **Docker Support** (For easy deployment)  
✅ **Cloud Deployment** (AWS, Render, or Heroku)

---

## 🏆 Contributing

Feel free to fork and contribute! Open an issue if you encounter any problems. 😊

---

## 📜 License

This project is **MIT Licensed**. Feel free to modify and use it as needed!
