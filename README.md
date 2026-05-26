#  Expense Tracker Web Application

A modern and user-friendly Expense Tracker web application built using Django. This project helps users manage daily expenses, track income, analyze spending habits, and maintain financial records efficiently through an interactive dashboard.

---

#  Live Demo

 https://expense-tracker-ld4c.onrender.com

---

#  Features

-  User Authentication System
-  User Profile Management
-  Add Income Records
-  Add Expense Records
-  Edit Expense & Income Details
-  Delete Records
-  Weekly Expense Reports
-  Monthly Expense Reports
-  Yearly Expense Analysis
-  Expense History Tracking
-  Dashboard Summary
-  Responsive UI Design
-  Cloud Deployment using Render

---

#  Technologies Used

## Backend
- Python
- Django

## Frontend
- HTML5
- CSS3
- Bootstrap 5
- JavaScript

## Database
- SQLite3

## Deployment & Server
- Render
- Gunicorn
- WhiteNoise

## Version Control
- Git
- GitHub

---

#  Project Structure

```bash
Expense-Tracker/
│
├── ExpenseTracker/
├── home/
├── templates/
├── static/
├── media/
├── staticfiles/
├── manage.py
├── requirements.txt
├── runtime.txt
├── build.sh
└── render.yaml
```

---

#  Installation Guide

##  Clone Repository

```bash
git clone https://github.com/Yashwanthx03/Expense-Tracker.git
cd Expense-Tracker
```

---

##  Create Virtual Environment

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### Mac/Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

---

##  Install Dependencies

```bash
pip install -r requirements.txt
```

---

##  Apply Database Migrations

```bash
python manage.py migrate
```

---

##  Create Superuser (Optional)

```bash
python manage.py createsuperuser
```

---

##  Collect Static Files

```bash
python manage.py collectstatic
```

Type:

```bash
yes
```

---

##  Run Development Server

```bash
python manage.py runserver
```

Application will run at:

```bash
http://127.0.0.1:8000/
```

---

#  Deployment on Render

This project is deployed using Render.

## Deployment Files Used

### runtime.txt

```txt
python-3.11.9
```

### Build Command

```bash
pip install setuptools==69.5.1 && pip install -r requirements.txt
```

### Start Command

```bash
gunicorn ExpenseTracker.wsgi --log-file -
```

---

#  Important Django Settings

```python
STATIC_URL = '/static/'

STATICFILES_DIRS = [
    os.path.join(BASE_DIR, 'static'),
]

STATIC_ROOT = os.path.join(BASE_DIR, 'staticfiles')

STATICFILES_STORAGE = 'whitenoise.storage.CompressedManifestStaticFilesStorage'

MIDDLEWARE = [
    'django.middleware.security.SecurityMiddleware',
    'whitenoise.middleware.WhiteNoiseMiddleware',
]

ALLOWED_HOSTS = [
    'expense-tracker-ld4c.onrender.com',
    '127.0.0.1'
]
```

---

#  Project Screenshots

##  Login Page

![Login Page](<img width="1264" height="589" alt="Images:login" src="https://github.com/user-attachments/assets/da79c322-cef7-4bd6-8a74-8ba689371399" />
)

---

##  Register Page

![Register Page](<img width="1260" height="591" alt="Images:register" src="https://github.com/user-attachments/assets/0061272a-2a81-4c53-9745-d48b685e5b64" />
)

---

##  Dashboard

![Dashboard](<img width="1266" height="592" alt="Images:dashboard" src="https://github.com/user-attachments/assets/f5c08d02-0dd3-48de-997e-f7a5a2a7464b" />
)

---

##  Add Expense Page

![Add Expense](<img width="1266" height="592" alt="Images:dashboard" src="https://github.com/user-attachments/assets/79e644c1-ee1d-4432-a4e5-c0e04a7e354a" />
)

---

##  History Page

![History](<img width="1280" height="568" alt="Images:history" src="https://github.com/user-attachments/assets/2373d5da-28d2-4422-8ad5-6577c4075446" />
)

---

#  Challenges Faced During Deployment

While deploying this project on Render, several issues were solved successfully:

- Static files not loading
- STATIC_ROOT configuration issue
- pkg_resources module error
- Python version compatibility issue
- cgi module error
- DisallowedHost error
- Gunicorn configuration problems
- Render root directory configuration

All deployment issues were debugged and fixed successfully.

---

#  What I Learned

Through this project, I learned:

- Django Project Structure
- User Authentication System
- CRUD Operations
- Template Rendering
- Static Files Management
- Django Deployment
- Git & GitHub Workflow
- Render Deployment Process
- Debugging Production Errors
- WhiteNoise Configuration
- Gunicorn Server Setup

---

#  Author

## Yashwanth

GitHub:
https://github.com/Yashwanthx03

---

#  Final Note

This project was built for learning full-stack Django development and deployment. It demonstrates backend development, frontend integration, database handling, authentication, static file management, and cloud deployment in a real-world project.
