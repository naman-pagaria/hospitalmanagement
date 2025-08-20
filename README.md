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

1. Clone the repo  
   git clone https://github.com/naman-pagaria/hospitalmanagement.git  
   cd hospitalmanagement  

2. Create a virtual environment (recommended)  
   python -m venv .venv  
   source .venv/bin/activate   (macOS/Linux)  
   .venv\Scripts\activate      (Windows)  

3. Install dependencies  
   pip install -r requirements.txt  

4. Setup database  
   python manage.py makemigrations  
   python manage.py migrate  

5. Run the server  
   python manage.py runserver  
   Visit: http://127.0.0.1:8000/

---

## 🔐 Demo Logins (for local testing)

**Admin**  
- user: admin  
- pass: 1234  

**Doctor**  
- user: doctor  
- pass: 1234  
(Doctor must be approved by Admin before login works)  

**Patients** (example set)  
- john_doe / 1234  
- jane_smith / 1234  
- michael_brown / 1234  
- emily_clark / 1234  
(Patients must be approved by Admin)

---

## 📧 Email (Contact Us) Configuration

If you use the Contact Us feature, set these in `hospitalmanagement/settings.py`:

EMAIL_HOST_USER = "your_email@gmail.com"  
EMAIL_HOST_PASSWORD = "your_app_password"  
EMAIL_RECEIVING_USER = "your_email@gmail.com"  

(For Gmail, create an **App Password** instead of using your real password.)

---

## 📁 Project Structure (high level)

hospitalmanagement/  
├── hospital/  
│   ├── static/hospital/  
│   ├── templates/hospital/  
│   ├── migrations/  
│   ├── models.py  
│   ├── views.py  
│   ├── forms.py  
│   └── ...  
├── hospitalmanagement/  
│   ├── settings.py  
│   ├── urls.py  
│   └── ...  
├── manage.py  
├── requirements.txt  
└── README.md  

---

## 📝 Notes & Limitations

- Admin signup is open (no approval). In production, restrict this or use Django superusers.  
- Ensure at least **one Doctor** exists before admitting patients.  
- Updating doctor/patient credentials may require resetting passwords.

---

## 🖼️ Screenshots (optional)

Add your images under `hospital/static/hospital/screenshots/` and update the links below.

| Homepage | Admin Dashboard | Invoice | Doctor List |
|---|---|---|---|
| ![Homepage](hospital/static/hospital/screenshots/homepage.png) | ![Admin Dashboard](hospital/static/hospital/screenshots/admin_dashboard.png) | ![Invoice](hospital/static/hospital/screenshots/invoice.png) | ![Doctor List](hospital/static/hospital/screenshots/admin_doctor.png) |

---

## 🤝 Contributing

PRs welcome! For major changes, please open an issue first to discuss what you’d like to change.

---

## ⚖️ License

MIT — see `LICENSE` for details.
