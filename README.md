# Django Todo CI/CD

A simple Todo application built with Django and integrated with a complete DevOps CI/CD workflow.

## Application

The Todo application allows users to create and manage their tasks through a simple web interface.

## Setup

Clone the repository:

```bash
git clone https://github.com/Irfan-devops1/django-todo-cicd.git
cd django-todo-cicd
```

Install Django and the required dependencies.

Create database migrations:

```bash
python manage.py makemigrations
```

Apply the migrations:

```bash
python manage.py migrate
```

Create an admin user:

```bash
python manage.py createsuperuser
```

Start the Django application:

```bash
python manage.py runserver
```

Open the application:

```text
http://127.0.0.1:8000/todos
```

## Docker

Build the Docker image:

```bash
docker build -t django-todo-app .
```

Run the application:

```bash
docker run -p 8000:8000 django-todo-app
```

Docker Compose can also be used:

```bash
docker compose up -d
```

## Kubernetes

Kubernetes deployment files are available in the `k8s/` directory.

The project includes:

* Deployment
* Pod
* Service
* MySQL Deployment
* MySQL Configuration
* MySQL Secret

Apply the Kubernetes resources:

```bash
kubectl apply -f k8s/
```

Check the resources:

```bash
kubectl get pods
kubectl get services
kubectl get deployments
```

## DevOps Implementation

This project was used to implement and practice a complete DevOps workflow including:

* Git & GitHub
* Jenkins CI/CD
* Docker
* Docker Compose
* Kubernetes
* Kubernetes deployment and services
* Containerized application deployment
* Automated build and deployment

## Project Structure

```text
django-todo-cicd/
│
├── Dockerfile
├── docker-compose.yml
├── manage.py
├── README.md
│
├── k8s/
│   ├── deployment.yaml
│   ├── pod.yaml
│   ├── service.yaml
│   └── MYSQL-DB/
│       ├── configMap.yml
│       ├── deployment.yml
│       └── secret.yml
│
├── todoApp/
│
├── todos/
│
└── staticfiles/
```

## Author

**Irfan Ahmad**

GitHub: https://github.com/Irfan-devops1

## License

This project includes the license provided with the original application. Please review `LICENSE` before redistributing or modifying the project.

