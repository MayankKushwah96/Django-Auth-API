# Django-Auth-API

This project is a user authentication and management system built with Django and Django REST framework. It supports user login, signup, password reset through email and normal methods, and includes an admin panel for managing users.

## Features

* User login and signup
* Password reset via email
* Normal password reset
* JWT authentication
* Admin panel with superuser creation

## Installation

### Clone the repository:
  * git clone https://github.com/your-username/your-repo-name.git
  * cd your-repo-name

### Create and activate a virtual environment:
  * python3 -m venv venv
  * source venv/bin/activate

### Set up environment variables:
#### Create a .env file in the project root and add the following:
  * EMAIL_USER='example123@gmail.com'
  * EMAIL_PASS='12345678'
  * EMAIL_FROM='example123@gmail.com'

### Run migrations:
  * python manage.py migrate

### Create a superuser:
  * python manage.py createsuperuser
  * --email your-email@example.com
  * --name your-name
  * --tc your-terms-and-conditions
  * --password your-password

## Configuration
1. In your settings.py file, ensure the apps are installed:
   
2. Add the settings for JWT authentication:
   
3. Configure email settings in settings.py:
  * EMAIL_BACKEND = "django.core.mail.backends.smtp.EmailBackend"EMAIL_HOST = 'smtp.gmail.com'
  * EMAIL_PORT = 587
  * EMAIL_HOST_USER = os.environ.get('EMAIL_USER')
  * EMAIL_HOST_PASSWORD = os.environ.get('EMAIL_PASS')
  * EMAIL_USE_TLS = True

4. Set password reset timeout:

5. Configure CORS settings:

## Usage:

1. Run the development server:
   * python manage.py runserver
     
2. Access the application:
   * User Signup http://localhost:8000/api/user/register
   * User Login http://localhost:8000/api/user/login
   * User Profile http://localhost:8000/api/user/profile
   * User Changepassword http://localhost:8000/api/user/changepassword
   * User Email Reset http://localhost:8000/api/user/send-reset-password-email/
   * User Password Reset http://localhost:8000/api/user/reset-password/<uid>/<token>/
   * Admin Panel at http://localhost:8000/admin/

     
