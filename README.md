# Template for Django Project Using Docker

## Stack
- Python
- Django
- PostgeSQL
- Gunicorn
- Nginx
- Docker

## Thanks to

[Michael Herman](https://testdriven.io/blog/dockerizing-django-with-postgres-gunicorn-and-nginx/#conclusion) for his tutorial

## Installation

- git clone https://github.com/erischon/django-project-template-docker.git .
- change Line Endings for entrypoint files : CRLF to LF
- add .env* to .gitignore
- Modify the README.md file ;)
- docker-compose exec web python manage.py startapp ...

Enjoy !

## Notes

- 

## Commands

### Development

- `docker-compose up -d --build`
- `docker-compose down -v`
- `docker-compose down`
- `docker-compose logs -f`
- `docker-compose exec web python manage.py createsuperuser`

### Production

- `docker-compose -f docker-compose.prod.yml up -d --build`
- `docker-compose -f docker-compose.prod.yml exec web python manage.py migrate --noinput`
- `docker-compose -f docker-compose.prod.yml exec web python manage.py collectstatic --no-input --clear`
- `docker-compose -f docker-compose.prod.yml down -v`
- `docker-compose -f docker-compose.prod.yml logs`