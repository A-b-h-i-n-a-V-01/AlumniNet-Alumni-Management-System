# 🎓 AlumniNet — Alumni Management System

> **B.Tech Semester 6 Mini Project**

AlumniNet is a web-based **Alumni Management System** developed to provide a centralized platform for connecting Alumni, Students, Faculty, and Administrators.

The system is designed to manage alumni information, improve communication, provide career opportunities, support networking, and maintain a structured alumni database.

---

## 📌 Project Overview

Maintaining alumni information through traditional methods can make it difficult for educational institutions to keep records updated and maintain continuous interaction with former students.

**AlumniNet** addresses this problem by providing a centralized digital platform where alumni information, career details, communication, job opportunities, events, and other activities can be managed efficiently.

The system provides different functionalities based on the user's role and uses role-based access control to ensure that users can access only the features relevant to them.

---

## 🎯 Objectives

- Create a centralized database for alumni information.
- Maintain alumni personal, academic, and career details.
- Connect Alumni, Students, Faculty, and Administrators.
- Provide a platform for communication and networking.
- Allow alumni to share career and job opportunities.
- Support faculty verification and moderation.
- Encourage alumni participation through a points and leaderboard system.
- Provide administrators with tools to manage the platform.

---

## ✨ Key Features

### 🔐 Role-Based Access Control

The system supports multiple user roles:

#### 👨‍🎓 Students
- Browse alumni directory
- View job opportunities
- Communicate with alumni
- Access relevant career information

#### 🎓 Alumni
- Create and manage professional profiles
- Share career information
- Post job opportunities
- Communicate with students and other alumni
- Earn points through contributions

#### 👨‍🏫 Faculty
- Monitor alumni-related activities
- Verify job postings
- Approve profiles and submitted content
- Moderate community content

#### 🛡️ Admin
- Manage users
- Manage approvals
- Moderate jobs and content
- View system statistics
- Manage the overall platform

---

## 💬 Communication

AlumniNet provides a private messaging system that allows users to communicate with each other.

Features include:

- One-to-one messaging
- Conversation history
- Unread message indicators
- Dynamic conversation handling

---

## 💼 Career & Job Opportunities

The platform provides a dedicated job and opportunity section.

Alumni can:

- Post job opportunities
- Provide job-related information
- Share opportunities with students

Students can:

- Browse available opportunities
- Filter job listings
- Explore career opportunities shared by alumni

Faculty and Admin users can moderate and verify job postings.

---

## 🏆 Gamification

AlumniNet includes a points-based contribution system.

Users can earn points through activities such as:

- Updating profiles
- Posting job opportunities
- Contributing to the alumni community

A **Leaderboard** displays contributor rankings and encourages active participation.

---

## 🖼️ Event Photo Sharing

The system provides a community gallery for alumni events and activities.

Features include:

- Uploading event photos
- Faculty moderation
- Approval-based publishing
- Community photo gallery

---

## 🛡️ Admin Panel

The administration section provides centralized control over the platform.

Administrators can manage:

- Users
- Alumni profiles
- Faculty approvals
- Job postings
- Community content
- Points
- System statistics

---

## 🛠️ Technologies Used

### Frontend
- HTML5
- CSS3
- JavaScript
- Bootstrap
- Jinja2 Templates

### Backend
- Python
- Flask
- Flask-WTF
- Flask-Login
- Flask-Bcrypt

### Database
- MySQL
- SQLAlchemy
- PyMySQL

### Development Tools
- Visual Studio Code
- Git
- GitHub

---

## 🏗️ System Architecture

```text
                    ┌─────────────────────┐
                    │       Users         │
                    │                     │
                    │ Student / Alumni    │
                    │ Faculty / Admin     │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │     Flask Web       │
                    │     Application     │
                    └──────────┬──────────┘
                               │
              ┌────────────────┼────────────────┐
              │                │                │
              ▼                ▼                ▼
        Authentication     Application      Role-Based
        & Authorization       Logic            Access
              │                │                │
              └────────────────┼────────────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │       MySQL         │
                    │      Database       │
                    └─────────────────────┘
```

---

## 📂 Project Structure

```text
AlumniNet-Alumni-Management-System/
│
├── app/
│   ├── static/
│   │   ├── css/
│   │   ├── js/
│   │   └── images/
│   │
│   ├── templates/
│   │   ├── admin_base.html
│   │   ├── admin_dashboard.html
│   │   ├── admin_faculty_approvals.html
│   │   ├── admin_jobs.html
│   │   ├── admin_login.html
│   │   ├── admin_points.html
│   │   ├── admin_stats.html
│   │   ├── admin_users.html
│   │   ├── base.html
│   │   ├── dashboard.html
│   │   ├── faculty_moderation.html
│   │   ├── jobs.html
│   │   ├── leaderboard.html
│   │   ├── login.html
│   │   ├── messages.html
│   │   ├── profile.html
│   │   ├── register.html
│   │   ├── search.html
│   │   ├── upload_photo.html
│   │   └── view_profile.html
│   │
│   ├── models.py
│   ├── routes.py
│   └── forms.py
│
├── config.py
├── run.py
├── setup_db.py
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation & Setup

### 1. Prerequisites

Make sure the following are installed:

- Python 3.8 or above
- MySQL Server
- Git

### 2. Clone the Repository

```bash
git clone https://github.com/abel-111/AlumniNet-Alumni-Management-System.git
cd AlumniNet-Alumni-Management-System
```

### 3. Create a Virtual Environment

#### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

#### Linux/macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🗄️ Database Setup

AlumniNet uses **MySQL** as its database.

Create the database using MySQL:

```sql
CREATE DATABASE alumni_platform;
```

The application uses the following database configuration:

```text
mysql+pymysql://root:root@localhost/alumni_platform
```

If your MySQL username or password is different, update the database configuration in the project accordingly.

---

## ▶️ Running the Application

Make sure the MySQL Server is running.

Then start the Flask application:

```bash
python run.py
```

The application will run at:

```text
http://127.0.0.1:5000
```

Open the URL in your web browser.

---

## 🗂️ Main Modules

| Module | Description |
|--------|-------------|
| Authentication | User registration and login |
| Alumni Directory | Search and view alumni profiles |
| Profiles | Manage personal and professional information |
| Jobs | Share and explore career opportunities |
| Messaging | Private communication between users |
| Leaderboard | Display contribution points |
| Event Gallery | Share alumni event photos |
| Faculty Moderation | Verify and moderate content |
| Admin Panel | Manage users and platform activities |

---

## 🗃️ Database Entities

The system contains database entities for managing:

- Users
- Alumni Profiles
- Student Profiles
- Faculty Profiles
- Skills
- Badges
- Certificates
- Messages
- Jobs
- Roadmaps
- Points
- Event Photos

---

## 🔒 Security

The application incorporates:

- Password hashing
- User authentication
- Role-based authorization
- Form validation
- Controlled access to administrative features
- Database-backed user management

---

## 🎓 Academic Project

### Project Title

**Digital Platform for Centralized Alumni Relationship and Management System**

### Project Name

**AlumniNet**

### Project Type

**B.Tech Semester 6 Mini Project**

### Project Domain

**Web Application / Alumni Relationship Management**

### Purpose

The project focuses on developing a centralized digital platform for managing alumni information and strengthening interaction between alumni, students, faculty, and the institution.

---

## 👨‍💻 Project Team

- **Abel Shibu**
- **Abhinav Krishna cs**
- **Akhil Shaji**
- **Aswin Soman**

---

## 📚 Learning Outcomes

Through this project, we gained practical experience in:

- Python programming
- Flask web application development
- MySQL database management
- SQLAlchemy ORM
- User authentication
- Role-based access control
- Frontend development
- Form validation
- Git and GitHub
- Full-stack web application development

---

## 🚀 Future Enhancements

Possible future improvements include:

- Mobile application support
- Email notifications
- Advanced alumni search
- Online event management
- Alumni recommendation system
- Enhanced analytics dashboard
- Cloud deployment
- Improved real-time communication

---

## 📄 License

This project was developed for academic purposes as part of a **B.Tech Semester 6 Mini Project**.

---

## ⭐ AlumniNet

**Connecting Alumni, Students and Institutions through a centralized digital platform.**
