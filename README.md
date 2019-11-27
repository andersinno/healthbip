# Health Bip

Django health checks for Kubernetes

## Installation

### PIP
`pip install healthbip`

### Poetry
`poetry add healthbip`

## Usage
Health Bip comes with two ways that is can be used. Either via URLs or via middleware,
the choice of installation is up to the user and both ways support being extended by
by subclassing the implementations.

### Add to Django apps
In your `DJANGO_APPS` settings, add `healthbip`.

```python
DJANGO_APPS = [
    ...,
    "healthbip",
    ...,
]
```


### URLs
In the projects main URL file, add the following:
```python
from healthblip.urls import health_urls

urlpatterns += health_urls
```

### Middleware
In the projects middleware settings, add the following:
```python
MIDDLEWARE = [
    "healthblip.middleware.HealthCheckMiddleware",
    ...,
]
```

Note that middleware ordering is taken into consideration when Django runs them, so the
higher up you place the middleware the earlier it will be evaluated.
