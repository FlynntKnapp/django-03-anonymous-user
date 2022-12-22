# Django AnonymousUser

## Process

1. [Create Django Project](./process/01_create_django_project.md)
1. [Add Django AdminDocs (`django.contrib.admindocs`) Application](./process/02_add_django_admindocs.md)
1. [Add User Login and Logout](./process/03_add_user_login_and_logout.md)
1. [Explore User Attributes and URL Routes](./process/04_explore_user_attributes_and_url_routes.md)

## Functional Code Example Repository

* <https://github.com/FlynntKnapp/django-anonymous-user>

## External Resources

### General

* [Django Login and Logout Tutorial - learndjango.com](https://learndjango.com/tutorials/django-login-and-logout-tutorial)
* [The Django admin documentation generator - `django.contrib.admindocs`](https://docs.djangoproject.com/en/4.1/ref/contrib/admin/admindocs/)

### `settings.py`

* [`INSTALLED_APPS`](https://docs.djangoproject.com/en/4.1/ref/settings/#installed-apps)
* [`TEMPLATES`](https://docs.djangoproject.com/en/4.1/ref/settings/#templates)
* [`TIME_ZONE`](https://docs.djangoproject.com/en/4.1/ref/settings/#time-zone)
* [`LOGIN_REDIRECT_URL`](https://docs.djangoproject.com/en/4.1/ref/settings/#login-redirect-url)
* [`LOGOUT_REDIRECT_URL`](https://docs.djangoproject.com/en/4.1/ref/settings/#logout-redirect-url)

### `urls.py`

* [`django.views.generic.base.TemplateView`](https://docs.djangoproject.com/en/4.1/ref/class-based-views/base/#django.views.generic.base.TemplateView)
* [`django.urls.path()`](https://docs.djangoproject.com/en/4.1/ref/urls/#path)
* [`django.urls.include()`](https://docs.djangoproject.com/en/4.1/ref/urls/#include)

### `template_name.html`

* [The Django template language](https://docs.djangoproject.com/en/4.0/ref/templates/language/)
* [The Django template language - `{{ VARIABLE }}`](https://docs.djangoproject.com/en/4.0/ref/templates/language/#variables)
* [The Django template language - `{% TAG %}`](https://docs.djangoproject.com/en/4.0/ref/templates/language/#tags)
  * [Built-in tag reference](https://docs.djangoproject.com/en/4.0/ref/templates/builtins/#built-in-tag-reference)
    * [`{% block %}`](https://docs.djangoproject.com/en/4.0/ref/templates/builtins/#block)
    * [`{% extends %}`](https://docs.djangoproject.com/en/4.0/ref/templates/builtins/#extends)
    * [`{% if %}`](https://docs.djangoproject.com/en/4.0/ref/templates/builtins/#if)
    * [`{% csrf_token %}`](https://docs.djangoproject.com/en/4.0/ref/templates/builtins/#csrf-token)
    * [`{% value | capfirst %}`](https://docs.djangoproject.com/en/4.0/ref/templates/builtins/#capfirst)

## Repository Links
