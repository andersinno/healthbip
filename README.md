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
