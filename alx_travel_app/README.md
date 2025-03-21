# ALX Travel App

A travel booking application with Celery integration for background tasks.

## Features
- Asynchronous email notifications using Celery
- RabbitMQ message broker integration
- Booking confirmation system

## Setup Instructions

1. Install Dependencies:
```bash
pip install celery rabbitmq-server django-celery-results
```

2. Configure RabbitMQ:
```bash
sudo service rabbitmq-server start
```

3. Start Celery Worker:
```bash
celery -A alx_travel_app worker -l info
```

## Environment Variables
Configure the following in settings.py:
- EMAIL_HOST_USER
- EMAIL_HOST_PASSWORD

## Testing
1. Create a booking through the API
2. Check Celery worker logs
3. Verify email receipt