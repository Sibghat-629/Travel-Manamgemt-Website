# ✈️ TravelMS — Travel Management Platform

![PHP](https://img.shields.io/badge/PHP-8%2B-777BB4?style=flat-square&logo=php)
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=flat-square&logo=mysql)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

A full-stack travel management platform designed to streamline trip planning, destination browsing, and secure booking management. Built with a PHP and SQL backend for robust data handling, featuring a dynamic and responsive user interface powered by HTML, CSS, and JavaScript.

---

## 📋 Table of Contents

- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Database Setup](#-database-setup)
- [Configuration](#-configuration)
- [Usage](#-usage)
- [Security](#-security)
- [Screenshots](#-screenshots)
- [Contributing](#-contributing)
- [License](#-license)

---

## ✨ Features

- **Destination Browser** — Explore and filter travel destinations with rich detail pages
- **Trip Planner** — Build and manage multi-stop itineraries with date and duration controls
- **Secure Booking System** — End-to-end booking flow with session-based authentication and input validation
- **User Authentication** — Register, login, and manage user profiles securely
- **Admin Dashboard** — Full CRUD management for destinations, users, and booking records
- **Responsive UI** — Mobile-first design that adapts seamlessly across all screen sizes
- **Search & Filter** — Dynamic search with real-time filtering powered by JavaScript
- **Booking History** — Users can view, manage, and cancel their bookings

---

## 🛠️ Tech Stack

| Layer      | Technologies                              |
|------------|-------------------------------------------|
| Backend    | PHP 8+, PDO, REST-style API endpoints     |
| Database   | MySQL 8.0, normalized relational schema   |
| Frontend   | HTML5, CSS3, Vanilla JavaScript, Fetch API|
| Server     | Apache, XAMPP / LAMP, `.htaccess` routing |
| Security   | PHP Sessions, `password_hash`, CSRF tokens, prepared statements |

---
# Application entry point
```

---


## 🚀 Getting Started

### Prerequisites

- PHP 8.0 or higher
- MySQL 8.0 or higher
- Apache server (XAMPP, WAMP, or LAMP stack)
- A web browser

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/travel-management.git
   ```

2. **Move to your server root**
   ```bash
   # For XAMPP (Windows)
   mv travel-management/ C:/xampp/htdocs/

   # For LAMP (Linux)
   mv travel-management/ /var/www/html/
   ```

3. **Set up the database** (see [Database Setup](#-database-setup) below)

4. **Configure your environment** (see [Configuration](#-configuration) below)

5. **Start Apache and MySQL** via XAMPP control panel or:
   ```bash
   sudo service apache2 start
   sudo service mysql start
   ```

6. **Visit the app** in your browser:
   ```
   http://localhost/travel-management/
   ```

---

## 🗄️ Database Setup

1. Open **phpMyAdmin** at `http://localhost/phpmyadmin` or use the MySQL CLI:
   ```bash
   mysql -u root -p
   ```

2. Create the database:
   ```sql
   CREATE DATABASE travel_management;
   ```

3. Import the schema:
   ```bash
   mysql -u root -p travel_management < sql/schema.sql
   ```

4. (Optional) Seed with sample data:
   ```bash
   mysql -u root -p travel_management < sql/seed.sql
   ```

---

## ⚙️ Configuration

1. Copy the example config file:
   ```bash
   cp config/db.example.php config/db.php
   ```

2. Edit `config/db.php` with your database credentials:
   ```php
   <?php
   define('DB_HOST', 'localhost');
   define('DB_NAME', 'travel_management');
   define('DB_USER', 'root');
   define('DB_PASS', 'your_password');
   ```

---

## 📖 Usage

### For Users
- Browse destinations on the home page
- Use the search bar to filter by location, price, or travel type
- Register or log in to create a booking
- View and manage your bookings from the profile page

### For Admins
- Navigate to `/admin/dashboard.php`
- Default admin credentials (change after first login):
  - **Email:** `admin@travelms.com`
  - **Password:** `Admin@1234`

---

## 🔒 Security

This platform implements the following security measures:

- **Password Hashing** — All passwords stored using `password_hash()` with `PASSWORD_BCRYPT`
- **Prepared Statements** — All database queries use PDO prepared statements to prevent SQL injection
- **CSRF Protection** — Forms include CSRF tokens validated on submission
- **Session Management** — Secure PHP sessions with regeneration on login
- **Input Validation** — Server-side validation on all user inputs
- **Access Control** — Role-based access restricts admin pages to authorized users only

---

## 📸 Screenshots

> Add screenshots of your application here.

| Home Page | Destination Detail | Booking Flow |
|-----------|-------------------|--------------|
| *(screenshot)* | *(screenshot)* | *(screenshot)* |

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Commit your changes: `git commit -m "Add your feature"`
4. Push to the branch: `git push origin feature/your-feature-name`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

<p align="center">Built with ❤️ using PHP · MySQL · HTML · CSS · JavaScript</p>
