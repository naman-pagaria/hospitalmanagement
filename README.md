# 🏥 Hospital Management System

[![Python](https://img.shields.io/badge/Python-3.11+-blue)]()
[![Django](https://img.shields.io/badge/Django-4.2-green)]()
[![License](https://img.shields.io/badge/License-MIT-lightgrey)]()

A full-stack **Django** app to manage hospital operations — patients, doctors, appointments, approvals, and billing.

---

## ✨ Features

### Admin
- Approve/reject **Doctors** and **Patients**
- Admit / discharge patients
- Approve / reject **Appointments**
- Generate & download **Invoice PDFs**
- Manage doctors & patients (update/delete)

### Doctor
- Apply for a job (requires admin approval)
- View assigned patients & their details
- See discharged patients
- View & manage own appointments

### Patient
- Sign up (requires admin approval)
- View assigned doctor details
- Book appointments (approval required)
- Download invoice after discharge

---

## 🧰 Tech Stack

- **Backend:** Django 4.2, Python 3.11
- **DB:** SQLite (dev)
- **Frontend:** Bootstrap 5, HTML, CSS
- **PDFs:** xhtml2pdf
- **Forms:** django-widget-tweaks

---

## 🚀 Quick Start

```bash
# 1) Clone
git clone https://github.com/naman-pagaria/hospitalmanagement.git
cd hospitalmanagement

# 2) Virtual env (recommended)
python -m venv .venv
source .venv/bin/activate        # macOS/Linux
# .venv\Scripts\activate         # Windows

# 3) Install deps
pip install -r requirements.txt

# 4) DB setup
python manage.py makemigrations
python manage.py migrate

# 5) Run
python manage.py runserver
# visit http://127.0.0.1:8000/
