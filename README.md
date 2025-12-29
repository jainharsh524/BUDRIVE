# BUDRIVE

**BUDRIVE** is a Django-based web application designed as a secure academic resource and file sharing platform. It enables users to register, authenticate, upload, and interact with academic content while offering administrators a comprehensive dashboard to manage users, files, and other resources.

---

## 🚀 Features

- User registration and authentication  
- Admin-controlled resource and user management  
- Upload and manage academic files/posts  
- Clean and extensible Django project structure  
- Uses Django’s built-in admin interface for backend operations  
- Media handling with WhiteNoise and Django static/media settings

---

## 📦 Tech Stack

| Layer | Technology |
|-------|------------|
| Backend | Django (Python) |
| Database | SQLite (default, easily replaceable) |
| Frontend | HTML, CSS, JavaScript |
| Authentication | Django Auth system |
| Static & Media | WhiteNoise, Django media settings |

---

## 🔧 Installation & Setup

Follow the steps below to run BUDRIVE locally:

1. **Clone the repository**

   ```bash
   git clone https://github.com/jainharsh524/BUDRIVE.git
   cd BUDRIVE```

2. **Create & activate a Python virtual environment**

   ```bash
   python3 -m venv venv
   source venv/bin/activate```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Apply database migrations**

   ```bash
   python manage.py migrate
   ```

5. **Create a superuser (admin access)**

   ```bash
   python manage.py createsuperuser
   ```

6. **Run the development server**

   ```bash
   python manage.py runserver
   ```

7. **Open in browser**

   Visit: `http://127.0.0.1:8000/`

---

## 🎯 Usage

| Feature          | URL                 |
| ---------------- | ------------------- |
| Admin Panel      | `/admin/`           |
| Login            | `/accounts/login/`  |
| Logout           | `/accounts/logout/` |
| Sign Up          | `/accounts/signup/` |
| Dashboard / Home | `/`                 |

> You may need to adjust URLs based on your custom routing in the project.

---

## 🗂️ Project Structure

```
BUDRIVE-main/
├── budrive/            # Django project + main app
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── ...
├── manage.py
├── db.sqlite3
├── requirements.txt
└── README.md
```

---

## 📝 Admin Panel Customization

BUDRIVE uses Django’s admin interface. You can customize:

* Admin display titles
* Model admin classes
* Dashboard organization

Example branding in `admin.py`:

```python
from django.contrib import admin

admin.site.site_header = "BUDRIVE Administration"
admin.site.site_title = "BUDRIVE Admin"
admin.site.index_title = "BUDRIVE Dashboard"
```

---

## 📌 Notes

* This setup uses **SQLite** by default. For production, configure a proper database like PostgreSQL.
* Static and media file handling is configured via WhiteNoise and Django’s media settings.
* Ensure to update `ALLOWED_HOSTS` before deploying.

---
## 🙋 Contributions

Contributions are welcome! To propose changes:

1. Fork this repository
2. Create your feature branch: `git checkout -b feature/xyz`
3. Commit your changes: `git commit -m "Add xyz"`
4. Push to branch: `git push origin feature/xyz`
5. Open a pull request

