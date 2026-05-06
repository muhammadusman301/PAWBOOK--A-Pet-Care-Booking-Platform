
# 🐾 PawBook - Pet Care Booking Platform

> **A centralized platform connecting pet owners with trusted service providers (groomers, walkers, sitters, and vets) across the UK.**

---

## 🎯 About the Project

**PawBook** is a comprehensive, dual-sided web application designed to revolutionize pet care services in the UK. It bridges the gap between pet owners seeking quality care and vetted service providers who can deliver it.

### Problem It Solves
- Difficulty finding trusted pet care providers
- Limited communication between owners and service providers
- Lack of detailed pet information sharing
- No centralized booking platform for multiple services

### Our Solution
A unified platform with:
- **Deep pet profiles** (60+ data points including medical history, behavioral triggers)
- **Smart booking workflow** with provider approval
- **Real-time communication** directly linked to bookings
- **Community ratings** from both owners and providers
- **Role-based dashboards** for different user types

---

## ✨ Key Features

### For Pet Owners
- 📱 **Detailed Pet Profiles**: Create comprehensive profiles with medical history, allergies, dietary needs, and behavioral notes
- 🔍 **Search & Browse**: Find vetted service providers near you (groomers, walkers, sitters, vets)
- 📅 **Smart Booking**: Propose times and dates; providers review your pet's profile before accepting
- 💬 **In-App Messaging**: Secure, real-time communication with providers for each booking
- ⭐ **Rate & Review**: Provide feedback on service quality

### For Service Providers
- 📊 **Professional Dashboard**: Manage all bookings and client relationships
- 👀 **Pet Profile Review**: See detailed pet information before accepting jobs
- 📋 **Job Management**: Accept/decline bookings with confidence
- 💬 **Direct Communication**: Message pet owners within the app
- ⭐ **Build Reputation**: Receive reviews and ratings from pet owners

### Platform Features
- 🔐 **JWT Authentication**: Secure login for all users
- 🌐 **CORS Support**: Seamless frontend-backend communication
- 🗄️ **SQLite Database**: Reliable data storage (Development)
- 📱 **Responsive UI**: Works on desktop and mobile devices

---

## 🛠️ Tech Stack

| Component | Technology | Version |
|-----------|-----------|---------|
| **Frontend** | React.js | 18.2.0 |
| **Styling** | Tailwind CSS | Latest |
| **Backend** | Django REST Framework | 3.14+ |
| **Language (Backend)** | Python | 3.8+ |
| **Database** | SQLite | (Development) |
| **Authentication** | JWT (SimpleJWT) | Latest |
| **API Format** | REST API | - |

### Why These Technologies?
- **React.js**: Modern, component-based UI development
- **Django REST Framework**: Robust backend with built-in features
- **Tailwind CSS**: Rapid UI development with utility-first CSS
- **SQLite**: Perfect for development; can upgrade to PostgreSQL for production

---

## ⚙️ Prerequisites

Before starting, ensure you have these installed on your system:

### Required Software

#### For Frontend Development:
- **Node.js** (v16.0.0 or higher)
- **npm** (comes with Node.js)

#### For Backend Development:
- **Python** (v3.8 or higher)
- **pip** (comes with Python)

### Check Your Installation

**Check Node.js:**
```bash
node --version   # Should show v16.0.0 or higher
npm --version    # Should show 8.0.0 or higher
```

**Check Python:**
```bash
python --version         # Should show Python 3.8+
python -m pip --version  # Should show pip version
```

### Don't Have These Installed?

**Install Node.js & npm:**
- Visit: https://nodejs.org/ (Download LTS version)
- Follow installation wizard

**Install Python:**
- Visit: https://www.python.org/downloads/
- Follow installation wizard
- ✅ **Important**: Check "Add Python to PATH" during installation

---

## 📁 Project Structure

```
Pet-Care-Booking-Platform/
│
├── client/                          # Frontend (React)
│   ├── public/                      # Static files
│   │   └── index.html              # Main HTML file
│   ├── src/                        # React components and pages
│   │   ├── components/             # Reusable UI components
│   │   ├── pages/                  # Page components
│   │   ├── App.js                  # Main App component
│   │   └── index.js                # Entry point
│   ├── package.json                # Frontend dependencies
│   └── package-lock.json           # Locked dependency versions
│
├── server/                          # Backend (Django)
│   ├── api/                        # Main API app
│   │   ├── models.py               # Database models
│   │   ├── views.py                # API endpoints logic
│   │   ├── serializers.py          # Data serialization
│   │   ├── urls.py                 # API routes
│   │   └── management/             # Custom commands
│   ├── core/                       # Django project settings
│   │   ├── settings.py             # Project configuration
│   │   ├── urls.py                 # Main URL routing
│   │   └── wsgi.py                 # WSGI application
│   ├── manage.py                   # Django management script
│   ├── db.sqlite3                  # Database (created after migration)
│   └── requirements.txt            # Python dependencies
│
└── README.md                        # This file
```

---

## 📦 Installation Guide (Step-by-Step)

### Step 1: Download Repo

Download the project then unzip it and then go to zip file (Pet-Care-Booking-Platform.zip) copy and paste on 
another location and unzip it and open cmd on this folder dir

---

### Step 2: Set Up the Backend (Python/Django)

#### 2a. Navigate to Server Directory
```bash
cd server
```

#### 2b. Create a Virtual Environment

A virtual environment isolates this project's dependencies from your system.

**On Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

**On macOS/Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

**How to know it worked:**
- Your terminal should show `(venv)` at the beginning of the line

#### 2c. Install Python Dependencies

```bash
pip install -r requirements.txt
```


#### 2d. Apply Database Migrations

Migrations set up the database structure:

```bash
python manage.py makemigrations
python manage.py migrate
```

**What this does:**
- Creates the SQLite database (`db.sqlite3`)
- Sets up all tables for users, pets, bookings, etc.

#### 2e. Create a Superuser (Admin Account)

```bash
python manage.py createsuperuser
```

**You'll be prompted for:**
- Username (e.g., `admin`)
- Email (e.g., `admin@example.com`)
- Password (enter and confirm)

---

### Step 3: Set Up the Frontend (React)

#### 3a. Open a New Terminal Window

Keep the backend terminal running. Open a new terminal/command prompt.

#### 3b. Navigate to Client Directory
```bash
cd client
```

#### 3c. Install Frontend Dependencies

```bash
npm install
```

**What this does:**
- Downloads React and all required packages
- Creates `node_modules` folder (this might take 1-2 minutes)

**What if it's slow?**
- This is normal the first time
- Subsequent installs will be faster due to caching

---

## ▶️ Running the Application

### Start the Backend Server

**In your first terminal (where you activated venv):**

```bash
python manage.py runserver
```

**Expected output:**
```
Starting development server at http://127.0.0.1:8000/
Press CTRL+C to quit.
```

✅ **Backend is running at:** `http://localhost:8000`

---

### Start the Frontend Server

**In your second terminal (in client directory):**

```bash
npm start
```

**Expected output:**
```
Compiled successfully!

You can now view pet-care-client in the browser.

  Local:            http://localhost:3000
  On Your Network:  http://192.168.x.x:3000
```

✅ **Frontend is running at:** `http://localhost:3000`

---

### Access the Application

**In your browser:**
- **Frontend App**: http://localhost:3000
- **Admin Panel**: http://localhost:8000/admin (use superuser credentials)
- **API**: http://localhost:8000/api

---

## 🔌 API Endpoints

### Base URL
```
http://localhost:8000/api/
```

### Authentication Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/auth/register/` | Register new user |
| `POST` | `/auth/login/` | Login and get JWT tokens |
| `POST` | `/auth/refresh/` | Refresh access token |

### Pet Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/pets/` | List all pets |
| `POST` | `/pets/` | Create a new pet |
| `GET` | `/pets/{id}/` | Get pet details |
| `PUT` | `/pets/{id}/` | Update pet |
| `DELETE` | `/pets/{id}/` | Delete pet |

### Service Provider Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/providers/` | List all providers |
| `GET` | `/providers/{id}/` | Get provider details |
| `PUT` | `/providers/{id}/` | Update profile |

### Booking Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/bookings/` | List your bookings |
| `POST` | `/bookings/` | Create booking |
| `GET` | `/bookings/{id}/` | Get booking details |
| `PUT` | `/bookings/{id}/` | Update booking status |

### Example API Call (Using cURL)

```bash
# Get all pets (requires authentication)
curl -H "Authorization: Bearer YOUR_TOKEN" \
  http://localhost:8000/api/pets/
```

---

## 🗄️ Database Models

### User Model
```
- username
- email
- password (hashed)
- first_name
- last_name
- user_type (owner/provider)
- created_at
```

### Pet Model
```
- name
- breed
- age
- weight
- medical_history
- allergies
- dietary_needs
- behavioral_notes
- owner (FK to User)
- created_at
```

### ServiceProvider Model
```
- user (FK to User)
- services_offered
- experience_years
- hourly_rate
- availability
- rating
- verified
```

### Booking Model
```
- pet (FK to Pet)
- provider (FK to ServiceProvider)
- owner (FK to User)
- service_type
- proposed_date_time
- status (pending/accepted/completed/cancelled)
- created_at
- updated_at
```

---

## 📂 File Structure Explanation

### Backend Structure

#### `server/core/settings.py`
- **Purpose**: Main configuration file for Django
- **Contains**: Database settings, installed apps, middleware, authentication settings
- **Don't touch**: Secret key and debug settings (change for production)

#### `server/api/models.py`
- **Purpose**: Defines the database structure
- **Contains**: Classes for User, Pet, ServiceProvider, Booking, etc.
- **What to do**: Add new models here when adding features

#### `server/api/views.py`
- **Purpose**: Handles API requests and returns responses
- **Contains**: Functions/classes that process incoming requests
- **What to do**: Create new views for new endpoints

#### `server/api/serializers.py`
- **Purpose**: Converts Python objects to JSON and vice versa
- **Contains**: Serializer classes for each model
- **Why needed**: Makes API responses clean and usable

#### `server/api/urls.py`
- **Purpose**: Maps URLs to views
- **Contains**: URL patterns for API endpoints
- **Example**: `/api/pets/` → `PetListView`

### Frontend Structure

#### `client/src/components/`
- **Purpose**: Reusable UI pieces
- **Examples**: Header, Button, Card, PetCard, etc.
- **Best practice**: Keep components small and focused

#### `client/src/pages/`
- **Purpose**: Full page components
- **Examples**: LoginPage, DashboardPage, BookingPage, etc.
- **Usage**: Usually mapped to routes

#### `client/src/App.js`
- **Purpose**: Main app component
- **Contains**: Routing logic, state management
- **What to do**: Add new routes here

#### `client/public/index.html`
- **Purpose**: Entry HTML file
- **Contains**: Root div where React mounts
- **Don't change**: Unless adding global styles/scripts

---

## 👥 Team

| Name | Role |
|------|------|
| **Muhammad Usman** | Backend Development, Database & APIs |
| **Huraira Tabassum** | Frontend UI & Dashboard Design |
| **Muhammad Nadeem Ashraf** | Business Logic & Authentication |
| **Abdul Hanan** | System Design & Documentation |
| **Muhammad Umer** | QA, Testing & Data Seeding |

---

## 📖 Additional Resources

- [Django Documentation](https://docs.djangoproject.com/)
- [Django REST Framework](https://www.django-rest-framework.org/)
- [React Documentation](https://react.dev/)
- [Tailwind CSS](https://tailwindcss.com/)
- [JWT Authentication](https://jwt.io/)

---

## 📝 License

This project is private and created by the team for educational purposes.

---
