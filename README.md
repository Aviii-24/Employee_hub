# 🧩 Employee_Hub

**Employee_Hub** is a Django REST Framework–based backend application designed to perform complete **CRUD operations** on employee data.  
It includes secure user registration, authentication, and RESTful endpoints for managing employee records.  
The project is live and deployed on Render.

🌐 **Live API:** [https://employee-hub-cgy3.onrender.com](https://employee-hub-cgy3.onrender.com)

---

## 🚀 Features

- ✅ User Registration & Login (Authentication)
- 🧠 JWT or Session-based Authentication (customizable)
- 📋 Create, Retrieve, Update, and Delete Employee Records
- 🔍 Get All Employees / Get Employee by ID
- ⚙️ Django REST Framework powered APIs
- 💾 MySQL Database Integration
- 🌐 Deployed on Render

---

## 🧱 Tech Stack

| Layer | Technology |
|-------|-------------|
| Backend | Django, Django REST Framework |
| Database | MySQL |
| Deployment | Render |
| Authentication | Django Auth / JWT (depending on your setup) |
| Language | Python 3.x |

---
## 🗂️ Folder Structure
```
EMPLOYEE_DJANGO_API/
│
├── employee/ # Main Django app
│ ├── migrations/
│ ├── init.py
│ ├── admin.py
│ ├── apps.py
│ ├── models.py
│ ├── serializers.py
│ ├── tests.py
│ ├── urls.py
│ └── views.py
│
├── employee_management/ # Django project settings
│ ├── init.py
│ ├── asgi.py
│ ├── settings.py
│ ├── urls.py
│ └── wsgi.py
│
├── myenv/ # Virtual environment (local)
├── db.sqlite3 # Local test database
├── Employee_API_Collection.postman_collection.json
├── initial_steup.txt
├── manage.py
├── Procfile # For Render deployment
└── requirements.txt
```

---

## 🔗 API Endpoints

| Method | Endpoint | Description |
|--------|-----------|-------------|
| `POST` | `/register` | Register a new user |
| `POST` | `/login` | Login existing user |
| `GET` | `/findByEmail?email=<email>` | Get employee by email |
| `GET` | `/getAll` | Retrieve all employees |
| `GET` | `/getById?id=<id>` | Retrieve employee by ID |
| `PUT` | `/update?id=<id>` | Update employee details |
| `DELETE` | `/delete?id=<id>` | Delete employee record |

> ⚠️ **Note:**  
> Some endpoints may expect parameters in the query string (`?id=` or `?email=`) depending on your `views.py` implementation.  
> Authentication is handled using Django’s built-in session authentication (not JWT).

---

## ⚙️ Setup Instructions (Local Development)

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/Employee_Hub.git
   cd Employee_Hub
 
2. **Create and activate a virtual environment**
   ```bash
   python -m venv venv
   venv\Scripts\activate     # Windows
   source venv/bin/activate  # macOS/Linux
   
3. **Install dependencies**
   ```bash
   pip install -r requirements.txt

4. **Configure Database**
  For local testing, you can use db.sqlite3 (already included).
  For MySQL, update employee_management/settings.py:

  ```
  DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'your_database_name',
        'USER': 'your_username',
        'PASSWORD': 'your_password',
        'HOST': 'your_host',
        'PORT': '3306',
      }
  }
 ```

5. **Run Migrations**
   ```bash
   python manage.py makemigrations
   python manage.py migrate

6.**Run Server**
  ```bash
  python manage.py runserver
```

🧩 Example JSON (Employee)
```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "position": "Software Engineer",
  "salary": 75000
}
```
📦 Deployment

This backend is deployed on Render using a Procfile for automated deployment.
👉 https://employee-hub-cgy3.onrender.com

🤝 Contributing

Contributions and suggestions are welcome!
Feel free to fork the repository and open pull requests.

👨‍💻 Author

Avinash Satalkar
💻 Django | REST Framework | Python | MySQL Developer
🔗 https://www.linkedin.com/in/avinash-satalkar-10a934230/
📧 avinash.satalkar2406@gmail.com

⭐ Show Support

If you found this project helpful, please give it a ⭐ on GitHub — it helps others discover it!
