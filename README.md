# 🎓 Campus Placement Portal

A web-based Campus Placement Portal built as **Task 5** of the Full Stack Web Development Internship at **ApexPlanet Software Pvt. Ltd.**

Students can register, browse job postings and apply for them, and track their application status. Admins can post and manage jobs and review and update applications.

## 🚀 Features

### 👨‍🎓 Student
- Registration and login
- Dashboard with job and application counts
- Browse available jobs
- Apply for jobs
- Track the status of applications

### 👨‍💼 Admin
- Admin dashboard (total students, jobs, applications, selected candidates)
- Add, view and delete job postings
- View all student applications
- Update application status (Pending / Selected / Rejected)

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | HTML5, CSS3, JavaScript |
| Backend | PHP (MySQLi, prepared statements, `password_hash`) |
| Database | MySQL |
| Environment | XAMPP, Visual Studio Code |

## 📂 Project Structure

```text
ApexPlanet-Task-5/
├── Campus Placement Portal/
│   └── Campus Placement Portal/
│       ├── admin/
│       │   ├── dashboard.php
│       │   ├── jobs.php
│       │   ├── add_job.php
│       │   ├── edit_job.php
│       │   ├── delete_job.php
│       │   └── applications.php
│       ├── student/
│       │   ├── dashboard.php
│       │   ├── jobs.php
│       │   ├── apply.php
│       │   └── applications.php
│       ├── database/
│       │   └── campus_placement.sql
│       ├── dp.php               # database connection
│       ├── create_admin.php     # one-time admin account creation
│       ├── index.php
│       ├── login.php
│       ├── register.php
│       ├── logout.php
│       ├── style.css
│       ├── script.js
│       └── er diagram.png
├── db.php, login.php, register.php, users.php, ...   # user management module
├── ER Diagram.jpeg
├── Campus_Placement_Portal_Project_Report.pdf
└── README.md
```

## ⚙️ Installation & Setup

1. **Install XAMPP** and start **Apache** and **MySQL**.
2. **Clone the repository** into `C:\xampp\htdocs\`:
```bash
   git clone https://github.com/<your-username>/ApexPlanet-Task-5.git
```
3. **Create the database.** Open `http://localhost/phpmyadmin` and import
   `Campus Placement Portal/Campus Placement Portal/database/campus_placement.sql`
   (it creates the `campus_placement` database).
4. **Check the DB connection** in `dp.php`:
```php
   $conn = new mysqli("localhost", "root", "", "campus_placement");
```
5. **Create the admin account.** Visit `create_admin.php` once in the browser, then delete or protect the file.
6. **Run the project:**
```text
   http://localhost/ApexPlanet-Task-5/ApexPlanet-Task-5-main/Campus Placement Portal/Campus Placement Portal/
```

> ⚠️ Change the default admin password after the first login, and do not deploy `create_admin.php` to a public server.

## 🔐 User Roles

| Role | Main functions |
|------|----------------|
| Student | Register, browse jobs, apply, track applications |
| Admin | Manage jobs, review applications, update status |

## 📊 Placement Workflow

```text
Student Registration → Login → Browse Jobs → Apply
        → Admin Reviews Application → Status Updated (Selected / Rejected)
```

## 🗄️ Database

The schema (`database/campus_placement.sql`) includes `users`, `students`, `companies`, `jobs`, `applications`, `interviews`, `notifications`, `password_resets` and `admin` tables. See `er diagram.png` and `ER Diagram.jpeg` for the ER diagram.

## 🔮 Future Enhancements
- Company/recruiter login and job posting
- Email/OTP verification and password reset
- Resume upload and student profile management
- Interview scheduling
- Advanced job search and filters
- Placement analytics dashboard

## 👩‍💻 Internship

**Internship:** Full Stack Web Development Internship
**Organization:** ApexPlanet Software Pvt. Ltd.
**Task:** Task 5 – Campus Placement Portal

## 📜 License

Developed for educational and internship purposes.
