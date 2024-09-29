# Flask-Login-MySQL-SessionManagement

A simple Flask-based login and registration system using MySQL for database management, with session handling via `app.secret_key`.

## Features:
- User login
- User registration
- Session management
- MySQL integration for storing user details

## Setup Instructions:

### 1. Clone the Repository:
```bash
git clone https://github.com/Gokul170601/Flask-Login-MySQL-SessionManagement.git
cd Flask-Login-MySQL-SessionManagement
```
### 2. Set up a Virtual Environment:
```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```
### 3.  Install Dependencies:
```bash
pip install -r requirements.txt
```
### 4. Configure MySQL:
- Ensure MySQL is installed and running.
- Create a database named `logindb`.
- Run the following SQL command to create the necessary table:
```
CREATE DATABASE IF NOT EXISTS `logindb`;
USE `logindb`;

CREATE TABLE `accounts` (
  `id` int NOT NULL AUTO_INCREMENT,
  `username` varchar(50) NOT NULL,
  `password` varchar(50) NOT NULL,
  `email` varchar(100) NOT NULL,
  PRIMARY KEY (`id`)
);
```
### 5. Set Up app.secret_key:
In app.py, replace app.secret_key = 'your_secret_key_here' with your actual secret key.

You can generate a secure key in Python:
```
import os
print(os.urandom(24))
```
### 6. Run the Flask App:
```bash
python run app.py
```
The application will be accessible at `http://localhost:5000`.

