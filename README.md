# Template for Django 4.2.3 using Docker (with Nginx, Gunicorn and PostgreSQL)

> I originally created this as a template for my own projects,
> but I decided to make it public in case anyone else finds it useful.
> Feel free to use it as a template for your own projects.
> If you have any suggestions for improvements, please let me know.
> I'm always looking for ways to improve my workflow.
>
> Thanks!
>
> "GeumJang Ahn" from South Korea

## Requirements

- Docker
- Docker Compose

## Installation

```
git clone
set .env ('/' and '/webapp')
```

## Commands

### nginx reload

```
docker exec -it nginx-dev-container nginx -s reload
```

### Build for Dev

```
docker-compuse up -d --build
```

### Build for Production

```
docker-compose -f docker-compose.production.yml up -d --build
```

### Log

```
docker-compose logs -f

docker-compose logs -f webapp
```

### Superuser

```
docker-compose run --rm webapp python manage.py createsuperuser
```
