# QR Based Food Ordering System

A web-based food ordering system built with **Django** and **MySQL** that allows restaurants to manage menus and tables while customers can scan QR codes, view the menu, and place food orders.

## 📌 Project Overview

The QR Based Food Ordering System is designed to simplify the food ordering process in restaurants.

Instead of waiting for a waiter to take an order, customers can scan a QR code associated with their table and access the restaurant's digital menu. The system provides separate functionality for restaurant management and customers.

### Main Workflow

```text
Customer
   │
   │ Scan QR Code
   ▼
Restaurant Menu
   │
   │ Select Food
   ▼
Place Order
   │
   ▼
Restaurant Receives Order
```

## ✨ Features

### Customer

* Scan restaurant/table QR code
* View restaurant menu
* View available food items
* Register and login
* Select food items
* Place food orders
* Use a digital ordering interface

### Restaurant

* Restaurant login
* Restaurant management screen
* Create and manage menu items
* Add/manage restaurant tables
* Generate QR codes
* View customer orders

### System

* Django-based web application
* MySQL database integration
* QR code generation
* Dynamic menu management
* Template-based web interface
* Environment-based configuration for sensitive credentials

## 🛠️ Technologies Used

| Technology    | Purpose                         |
| ------------- | ------------------------------- |
| Python        | Programming language            |
| Django 3.2    | Web framework                   |
| MySQL         | Database                        |
| PyMySQL       | MySQL connectivity              |
| PyQRCode      | QR code generation              |
| pypng         | PNG generation for QR codes     |
| HTML/CSS      | Frontend                        |
| python-dotenv | Environment variable management |

## 📂 Project Structure

```text
QR Based Food Ordering System/
│
├── manage.py
├── requirements.txt
├── .gitignore
├── .env                    # Not committed to GitHub
│
├── FoodOrdering/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
│
└── FoodOrderingApp/
    ├── __init__.py
    ├── admin.py
    ├── apps.py
    ├── models.py
    ├── urls.py
    ├── views.py
    ├── tests.py
    │
    ├── migrations/
    │
    ├── templates/
    │   ├── index.html
    │   ├── Login.html
    │   ├── Register.html
    │   ├── CreateMenu.html
    │   ├── AddChairs.html
    │   ├── ScanQR.html
    │   ├── RestaurantScreen.html
    │   └── UserScreen.html
    │
    └── static/
        ├── images/
        ├── menus/
        └── qrcodes/
```

## ⚙️ Requirements

Make sure the following are installed:

* Python 3.10
* MySQL Server
* pip
* Git

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Akashbuddha/QR-based-food-ordering-system.git
```

Move into the project directory:

```bash
cd QR-based-food-ordering-system
```

### 2. Create a Virtual Environment

Windows:

```powershell
python -m venv venv
```

Activate it:

```powershell
venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

## 🗄️ Database Configuration

Create a MySQL database named:

```text
foodordering
```

For example, using MySQL:

```sql
CREATE DATABASE foodordering;
```

Make sure your MySQL server is running before starting Django.

## 🔐 Environment Variables

Create a `.env` file in the same directory as `manage.py`.

```env
SECRET_KEY=your_django_secret_key

DB_NAME=foodordering
DB_USER=root
DB_PASSWORD=your_mysql_password
DB_HOST=127.0.0.1
DB_PORT=3306
```

### Important

Never commit `.env` to GitHub.

The `.gitignore` file should contain:

```gitignore
.env
__pycache__/
*.pyc
venv/
.venv/
env/
*.log
.vscode/
.idea/
Thumbs.db
```

## 🔄 Database Migration

After configuring MySQL, run:

```bash
python manage.py makemigrations
```

Then:

```bash
python manage.py migrate
```

## ▶️ Run the Application

Start the Django development server:

```bash
python manage.py runserver
```

Open your browser and visit:

```text
http://127.0.0.1:8000/
```

## 👤 Creating an Admin User

To create a Django administrator account:

```bash
python manage.py createsuperuser
```

Follow the prompts to enter the username, email, and password.

The Django admin panel can normally be accessed at:

```text
http://127.0.0.1:8000/admin/
```

## 🔗 QR Code Workflow

The system uses QR codes to connect restaurant tables with the digital ordering interface.

```text
Restaurant
    │
    ├── Add Table
    │
    ├── Generate QR Code
    │
    └── Assign QR Code to Table
                │
                ▼
             Customer
                │
                ▼
          Scan QR Code
                │
                ▼
          View Menu
                │
                ▼
          Place Order
                │
                ▼
          Restaurant
```

## 🔒 Security

The project uses environment variables for sensitive configuration.

Sensitive information such as:

* Django `SECRET_KEY`
* MySQL password
* Database credentials

should not be committed to the repository.

Before pushing code to GitHub, verify:

```bash
git status
```

and make sure `.env` is not included in the commit.

## 🧪 Django System Check

You can verify the Django configuration with:

```bash
python manage.py check
```

A successful configuration should display:

```text
System check identified no issues (0 silenced).
```

## 📦 Dependencies

The project uses the following Python packages:

```text
Django==3.2
PyMySQL==1.1.2
PyQRCode==1.2.1
pypng==0.20220715.0
python-dotenv==1.2.3
```

Install all dependencies using:

```bash
pip install -r requirements.txt
```

## 🎯 Project Objective

The objective of this project is to provide a simple digital restaurant ordering system that reduces manual ordering and provides customers with a QR-based way to access restaurant menus and place orders.

## 🔮 Future Enhancements

Possible future improvements include:

* Online payment integration
* Order status tracking
* Restaurant analytics dashboard
* Customer order history
* Real-time order notifications
* Mobile application
* Cloud deployment
* Role-based access control
* Improved responsive UI
* Docker-based deployment

## 👨‍💻 Author

**Akash Buddha**

GitHub:

https://github.com/Akashbuddha

## 📄 License

This project is intended for educational and project-development purposes.
