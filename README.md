# Flask Bootstrap App

This is a simple Flask application that utilizes Bootstrap 5 to create a beautiful user interface. The application serves as a starting point for building web applications with Flask and Bootstrap.


## Features

- Responsive Bootstrap 5 UI
- Add, complete, and delete todos
- MySQL database integration
- Environment variable support via `.env`
- Easy deployment and logging

## Prerequisites

- Python 3.9+
- MySQL server
  (Download it from https://dev.mysql.com/downloads/installer/)
- pip (Python package manager)

## Use this Command to Create new user

```CREATE USER 'admin'@'localhost' IDENTIFIED WITH mysql_native_password BY 'Secret123!';
GRANT ALL PRIVILEGES ON *.* TO 'admin'@'localhost' WITH GRANT OPTION;
CREATE USER 'admin'@'%' IDENTIFIED WITH mysql_native_password BY 'Secret123!';
GRANT ALL PRIVILEGES ON *.* TO 'admin'@'%' WITH GRANT OPTION;
FLUSH PRIVILEGES;
```

## Setup Instructions

### 1. Clone the Repository

```bash
git clone <your-repo-url>
cd flask-bootstrap-app
```

### 2. Create the `.env` File

Create a `.env` file in the project root with your configuration:

```
SECRET_KEY=your_secret_key
MYSQL_HOST=localhost
MYSQL_USER=root
MYSQL_PASSWORD=your_password
MYSQL_DB=july25_todo_app
APP_PORT=5000
```

### 3. Install System Dependencies

For Ubuntu/Debian:

```bash
sudo apt-get update
sudo apt-get install -y python3 python3-pip default-libmysqlclient-dev build-essential pkg-config mysql-client
```

### 4. Install Python Dependencies

```bash
pip3 install --break-system-packages -r requirements.txt
```

### 5. Create the MySQL Database

```bash
mysql -hlocalhost -uroot -p'your_password' -e "CREATE DATABASE IF NOT EXISTS july25_todo_app;"
```

### 6. Run the Application

For demo/development:

```bash
python3 app.py
```

For background/production:

```bash
nohup python3 app.py > app.log 2>&1 &
```

### 7. Access the App

Open your browser and go to:

```
http://<server-ip>:5000
```

## Logs

To view logs:

```bash
tail -f app.log
```

## Security

- **Do not commit your `.env` file to source control.**
- Use firewalls and security groups to restrict access to your app port.

## License





MIT
