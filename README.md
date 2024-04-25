# Project Setup Guide

This guide will help you set up the project environment, including backend and frontend dependencies, as well as the database.

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

3. Install backend project dependencies:
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

## Step 3: Backend Migration

1. Make migrations:
    ```bash
    python manage.py makemigrations
    ```

2. Apply migrations:
    ```bash
    python manage.py migrate
    ```

## Step 4: Frontend Setup

1. Navigate to the frontend directory:
    ```bash
    cd frontend
    ```

2. Install frontend dependencies using npm:
    ```bash
    npm install
    ```

## Step 5: Run the Server

Start the Django server:
```bash
python manage.py runserver
## Step 6: Run the frontend
```bash
npm start

