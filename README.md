# 🐍 FLASK_APP

A modular Flask-based backend application with MQTT integration, MySQL database support, structured logging, and comprehensive test coverage.

---

## 📂 Project Structure

```
FLASK_APP/
│
├── Employee/               # Employee module (routes, models, logic)
├── Todo/                   # Todo module (routes, models, logic)
├── migrations/             # Database migration files
├── templates/              # HTML templates (Jinja2)
├── tests/                  # Test suite (98%+ coverage)
│
├── app.py                  # Application entry point
├── db.py                   # Database connection & setup
├── logger.py               # Logging configuration
├── mqtt_local.py           # MQTT client integration
├── mysql_configuration.py  # MySQL config loader
├── requirement.txt         # Python dependencies
└── .coverage               # Test coverage report
```

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/VIKAS231101/FLASK_APP.git
cd FLASK_APP
```

### 2. Create & Activate Virtual Environment

```bash
python -m venv myenv

myenv\Scripts\activate      # Windows
# source myenv/bin/activate # Mac/Linux
```

### 3. Install Dependencies

```bash
pip install -r requirement.txt
```

### 4. Configure MySQL

Update `mysql_configuration.py` with your database credentials:

```python
DB_HOST     = "localhost"
DB_USER     = "your_user"
DB_PASSWORD = "your_password"
DB_NAME     = "your_database"
```

### 5. Run Migrations

```bash
flask db upgrade
```

### 6. Start the App

```bash
python app.py
```

App runs on: http://127.0.0.1:5000

---

## 🔌 Modules

### 👤 Employee
Handles employee management — create, read, update, and delete employee records.

### ✅ Todo
Manages todo items — task creation, status tracking, and deletion.

---

## 📡 MQTT Integration

The app integrates with an MQTT broker via `mqtt_local.py` for real-time messaging support.

Configure your broker settings inside `mqtt_local.py`:

```python
BROKER_HOST = "localhost"
BROKER_PORT = 1883
TOPIC       = "your/topic"
```

---

## 🧪 Testing

```bash
pytest tests/
```

Run with coverage report:

```bash
pytest --cov=. tests/
```

> ✅ Current test coverage: **98%**

---

## 📋 Logging

All application events are captured via `logger.py` and written to `log_file.txt` for easy debugging and monitoring.

---

## 🔐 Security Practices

- No hardcoded credentials — config loaded via dedicated config files
- Virtual environment excluded from version control
- Sensitive files should be added to `.gitignore`

---

## 🚀 Future Improvements

- 🔐 JWT-based authentication
- 🐳 Docker support
- 📄 Swagger / OpenAPI documentation
- 🌐 REST API versioning
- 📊 Analytics & reporting dashboard

---

## 👤 Author

**VIKAS231101** — [GitHub](https://github.com/VIKAS231101)
