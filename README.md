# 🏥 Hospital Management System

[![Python](https://img.shields.io/badge/Python-3.11+-blue)]()
[![Django](https://img.shields.io/badge/Django-4.2-green)]()
[![Bootstrap](https://img.shields.io/badge/Bootstrap-5-purple)]()
[![License](https://img.shields.io/badge/License-MIT-lightgrey)]()

A full-stack **Django application** for managing hospital operations — patients, doctors, appointments, approvals, and billing — built for learning and demonstration purposes.

---

## ✨ Features

### 👨‍💼 Admin
- Create an account & login (auto-approved)
- Approve/reject **Doctors** and **Patients**
- Admit & discharge patients
- Approve/reject **Appointments**
- Generate & download **Invoice PDFs**
- Manage doctors & patients (update/delete)

### 👨‍⚕️ Doctor
- Apply for a job (requires admin approval)
- View assigned patients & details
- See discharged patients
- Manage own appointments

### 🧑‍🤝‍🧑 Patient
- Sign up (requires admin approval)
- View assigned doctor’s details
- Book appointments (approval required)
- Download invoice after discharge

---

## 🧰 Tech Stack

- **Backend:** Django 4.2, Python 3.11
- **Database:** SQLite (default, easy to run locally)
- **Frontend:** HTML, CSS, Bootstrap 5
- **PDF Generation:** xhtml2pdf
- **Form Enhancements:** django-widget-tweaks

---

## 🚀 Quick Start

1. Clone the repository
   - `git clone https://github.com/naman-pagaria/hospitalmanagement.git`
   - `cd hospitalmanagement`

2. Create virtual environment (recommended)
   - `python -m venv .venv`
   - `source .venv/bin/activate` (macOS/Linux)
   - `.venv\Scripts\activate` (Windows)

3. Install dependencies
   - `pip install -r requirements.txt`

4. Setup database
   - `python manage.py makemigrations`
   - `python manage.py migrate`

5. Run server
   - `python manage.py runserver`
   - Open `http://127.0.0.1:8000/`

---

## 🔑 Demo Logins

| Role   | Username | Password   |
|--------|----------|------------|
| Admin  | admin    | admin123   |
| Doctor | doctor1  | doctor123  |
| Patient| patient1 | patient123 |

---

## 📸 Screenshots

### Homepage
![Homepage](static/screenshots/homepage.png)

### Admin Dashboard
![Admin Dashboard](static/screenshots/admin_dashboard.png)

### Doctor List
![Doctor List](static/screenshots/admin_doctor.png)

### Invoice
![Invoice](static/screenshots/invoice.png)

---

## ⚙️ Configuration Notes

For the **Contact Us** form to work, update your `settings.py` with a Gmail account:



👉 Make sure **Less Secure Apps** (or App Passwords if 2FA is on) is enabled in your Gmail.

---

## 🚧 Known Limitations

- Any user can register as Admin (no approval).  
  ➝ Suggested: disable public admin signup, use Django superuser.
- At least one Doctor must exist before admitting a patient.
- On updating a Doctor/Patient, password must also be updated.

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## 🙋 Feedback & Contributions

Contributions, suggestions, and feedback are always welcome!  
Feel free to fork this repo and raise a PR 🚀
