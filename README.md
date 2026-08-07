# Django Basic

A beginner-friendly Django application demonstrating the fundamentals of web development with Django, Docker, and MySQL.

## Features

* Django web framework
* Dockerized application
* MySQL database integration
* Environment variable configuration using `.env`
* Docker Compose for multi-container setup
* Modular Django application structure

## Tech Stack

* Python 3.12
* Django
* MySQL 8
* Docker
* Docker Compose

## Project Structure

```text
Django Basic/
│
├── employees/             # Django application
├── mysite/                # Project configuration
├── media/                 # Uploaded media files
├── templates/             # HTML templates
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
├── manage.py
├── .env
└── README.md
```

## Prerequisites

Before running the project, ensure the following are installed:

* Python 3.12 (for local development)
* Docker Desktop
* Docker Compose
* Git

## Environment Variables

Create a `.env` file in the project root.

Example:

```env
SECRET_KEY=your-secret-key
DEBUG=True

DB_NAME=employee_db
DB_USER=root
DB_PASSWORD=root
DB_HOST=mysql
DB_PORT=3306
```

## Running the Project with Docker

### Build the Docker image

```bash
docker compose build
```

### Start the containers

```bash
docker compose up
```

or rebuild automatically after changes:

```bash
docker compose up --build
```

### Run in detached mode

```bash
docker compose up -d
```

### Stop the application

```bash
docker compose down
```

## Running Database Migrations

```bash
docker compose exec django python manage.py makemigrations
docker compose exec django python manage.py migrate
```

## Create a Superuser

```bash
docker compose exec django python manage.py createsuperuser
```

## Run the Development Server

If using Docker Compose, Django will be available at:

```
http://localhost:8000
```

## Common Docker Commands

### View running containers

```bash
docker ps
```

### View logs

```bash
docker compose logs
```

### View logs for Django only

```bash
docker compose logs django
```

### Restart containers

```bash
docker compose restart
```

### Stop containers

```bash
docker compose down
```

### Rebuild the image

```bash
docker compose build --no-cache
```

## Project Workflow

1. Clone the repository.
2. Create the `.env` file.
3. Build the Docker image.
4. Start the containers.
5. Apply database migrations.
6. Create a Django superuser.
7. Open the application in your browser.

## Learning Objectives

This project demonstrates:

* Django project structure
* Django applications
* Models and migrations
* URL routing
* Dockerfile creation
* Docker Compose configuration
* MySQL integration with Django
* Environment variable management
* Containerized application deployment

## Future Enhancements

* Django REST Framework APIs
* User authentication
* CRUD operations
* Static and media file handling
* Nginx reverse proxy
* Gunicorn for production deployment
* CI/CD pipeline
* Unit and integration tests

## License

This project is intended for learning and educational purposes.
