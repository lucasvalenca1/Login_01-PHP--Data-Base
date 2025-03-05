# PHP Login System

<p align="center">
  <img src="https://www.php.net/images/logos/new-php-logo.svg" width="200" alt="PHP Logo">
  <img src="https://www.mysql.com/common/logos/logo-mysql-170x115.png" width="150" alt="MySQL Logo">
</p>

---

## About This Project
A secure PHP login system demonstrating user authentication, registration, and session management using MySQL. Features include:

- User registration with password hashing
- Login/logout functionality
- Session-based authentication
- Profile management
- Basic dashboard for authenticated users

---

## Features
- **User Registration**: Secure account creation with password hashing
- **Login/Logout**: Session-based authentication system
- **Profile Management**: Update user details
- **Security**: Protection against SQL injection & XSS attacks
- **Responsive Design**: Works on desktop and mobile devices

---

## Screenshots
![Registration Page](screenshots/register.png)
![Login Page](screenshots/login.png)
![User Dashboard](screenshots/dashboard.png)

---

## Installation

### Requirements
- Web server (Apache/Nginx)
- PHP 7.4+
- MySQL 5.7+

### Setup Steps
1. **Clone Repository**
git clone https://github.com/lucasvalenca1/php-login-system.git

text

2. **Create Database**
CREATE DATABASE php_login;
USE php_login;

CREATE TABLE users (
id INT PRIMARY KEY AUTO_INCREMENT,
username VARCHAR(50) UNIQUE NOT NULL,
email VARCHAR(100) UNIQUE NOT NULL,
password VARCHAR(255) NOT NULL,
created_at DATETIME DEFAULT CURRENT_TIMESTAMP
);

text

3. **Configure Database**
Create `config.php` from sample:
cp config.sample.php config.php

text
Update with your database credentials:
define('DB_HOST', 'localhost');
define('DB_USER', 'root');
define('DB_PASS', 'your_password');
define('DB_NAME', 'php_login');

text

4. **Access Application**
http://localhost/php-login-system

text

---

## Usage
1. **Register**: Create a new account
2. **Login**: Use your credentials to access the dashboard
3. **Profile**: Update your account details
4. **Logout**: End your session securely

---

## Security Features
- Password hashing using PHP `password_hash()`
- Prepared statements for database queries
- Session timeout (30 minutes inactivity)
- CSRF protection
- Input validation/sanitization

---

## File Structure
php-login-system/
├── includes/
│ ├── config.php
│ ├── auth.php
│ └── database.php
├── public/
│ ├── register.php
│ ├── login.php
│ └── dashboard.php
├── assets/
│ ├── css/
│ └── js/
└── README.md

text

---

## Technologies Used
- **Backend**: PHP 8
- **Database**: MySQL
- **Frontend**: HTML5, CSS3, JavaScript
- **Security**: PHP password_hash(), prepared statements

---

## Contributing
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## License
Distributed under the MIT License. See `LICENSE` for more information.

---
