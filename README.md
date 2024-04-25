# 3-tier
# Project Setup Guide

This guide will help you set up the project environment and database.

## Step 1: Environment Setup

### Linux
1. Create a virtual environment:
    ```bash
    python -m venv env
    ```

2. Activate the virtual environment:
    ```bash
    source env/bin/activate
    ```

3. Install project dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Step 2: Database Setup

1. Access MySQL shell:
    ```bash
    mysql -u root -p
    ```

2. Create a new user:
    ```sql
    CREATE USER 'user'@'localhost' IDENTIFIED BY 'root';
    ```

3. Grant privileges to the user:
    ```sql
    GRANT ALL PRIVILEGES ON *.* TO 'root'@'localhost' WITH GRANT OPTION;
    ```

4. Create a new database:
    ```sql
    CREATE DATABASE userdb;
    ```

5. Switch to the new database:
    ```sql
    USE userdb;
    ```

6. Insert sample data into the user table:
    ```sql
    INSERT INTO myapp_user (user) VALUES ('John');
    ```

7. Exit MySQL shell:
    ```sql
    EXIT;
    ```

## Step 3: Migration

1. Make migrations:
    ```bash
    python manage.py makemigrations
    ```

2. Apply migrations:
    ```bash
    python manage.py migrate
    ```

## Step 4: Run the Server

Start the Django server:
```bash
python manage.py runserver


