# Vehicle-Parking-App
It is a multi-user app (one requires an administrator and other users) that manages different parking lots, parking spots and parked vehicles. This parking app is for car and bike parking only.

# Vehicle Parking App (VIPSpot)

A Flask-based web application to manage vehicle parking with two roles:
- **Admin**: Manages parking lots and parking spots.
- **User**: Can reserve and release parking spots.

### Admin:
- Login with hardcoded credentials.
- Add, edit, delete parking lots and spots.
- View all users.
- Search parking lots.
- Dashboard summary with charts.

### User:
- Register and log in.
- View available parking lots and spots.
- Book and release a parking spot.
- View reservations.

## Folder Structure

```
MAD_I_Project/
│
├── app.py                     # Entry point
├── controllers/               # Contains admin and user route logic
│   ├── admin_controller.py
│   └── user_controller.py
│
├── models/                    # Database models
│   └── db_model.py
│
├── templates/                 # HTML templates (Jinja2)
│   └── ...
│
├── static/                    # CSS, JS, and images
│
├── database/parking.db        # SQLite database (generated automatically)
│
└── README.md
```

## Prerequisites

- Python 3.8 or higher
- pip (Python package manager)
- (Optional but recommended) virtualenv

## Setup Instructions

### 1. Clone or unzip the project

```bash
cd MAD_I_Project
```

### 2. (Optional) Create and activate virtual environment

```bash
python -m venv venv
source venv/bin/activate      # On Linux/Mac
venv\Scripts\activate         # On Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

If `requirements.txt` is missing, manually install:

```bash
pip install flask flask-login flask_sqlalchemy
```

## Running the App

```bash
python app.py
```

App will be available at: [http://127.0.0.1:5000](http://127.0.0.1:5000)

## 🔑 Admin Credentials

```
Email:    admin.vipspot@email.com
Password: admin@vipspot
```

## Notes

- The database (`parking.db`) is automatically created on first run.
- Admin has fixed login — no registration.
- Users must register and then log in to use the system.
