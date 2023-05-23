# OrbStack Issues Repro

## Intro

Before I used OrbStack, I already made a composer for the Django application for automatic deployment, after using OrbStack my composer doesn't work anymore, so I'm making a repro to test out this situation.

## Environment

- Django
- Python
- Docker

## Usage

```bash
cp example-env .env
docker-compose up -d
```

## Modifcation

I removed the database part in the docker-compose.yml
Also removed the Internal network interface

# Result

I can not reproduce the issue, the composer works fine.

# Reference

- [django-composer-example](https://github.com/ZoneTwelve/django-composer-example)
- [OrbStack Documentation](https://docs.orbstack.dev/install#colima-context)