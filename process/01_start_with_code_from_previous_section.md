# Start with Code from Repository of Previous Section

* [Django Admin Documentation Generator](https://github.com/FlynntKnapp/django-admin-documentation-generator)
* You can even copy or clone your previous code/repository to start this next section or you can start from scratch.

## Assumptions

1. Project is starting with a functioning Django project called [`config`](../config/) with modified [`config/settings.py`](../config/settings.py) file and [`config/urls.py`](../config/urls.py) file:
    * `ls config`:
    * Sample [`config`](../config/) directory contents:

        ```console
        PS C:\Users\FlynntKnapp\Programming\03-django-anonymous-user> ls config   

            Directory: C:\Users\FlynntKnapp\Programming\03-django-anonymous-user\config

        Mode                 LastWriteTime         Length Name
        ----                 -------------         ------ ----
        -a---          12/18/2022 11:18 AM              0 __init__.py
        -a---          12/18/2022 11:18 AM            405 asgi.py
        -a---          12/18/2022  8:56 PM           3473 settings.py
        -a---          12/18/2022  7:56 PM           1039 urls.py
        -a---          12/18/2022 11:18 AM            405 wsgi.py

        PS C:\Users\FlynntKnapp\Programming\03-django-anonymous-user>
        ```

1. Project has [`manage.py`](../manage.py) file in the root directory:
    * `ls manage.py`:
    * Sample root directory contents:

        ```console
        PS C:\Users\FlynntKnapp\Programming\03-django-anonymous-user> ls manage.py

            Directory: C:\Users\FlynntKnapp\Programming\03-django-anonymous-user

        Mode                 LastWriteTime         Length Name
        ----                 -------------         ------ ----
        -a---          12/18/2022 11:18 AM            684 manage.py

        PS C:\Users\FlynntKnapp\Programming\03-django-anonymous-user>
        ```

1. Project already has an appropriate [`config/urls.py`](../config/urls.py) file with `urlpatterns` for `admindocs` and `admin`:
    * Sample file contents:

        ```python
        from django.contrib import admin
        from django.urls import path, include

        urlpatterns = [
            #...
            path('admin/doc/', include('django.contrib.admindocs.urls')),
            path('admin/', admin.site.urls),
            #...
        ]
        ```

1. Project already has the [`admindocs`](https://docs.djangoproject.com/en/4.1/ref/contrib/admin/admindocs/) app listed in `INSTALLED_APPS` list in [`config/settings.py`](../config/settings.py):
    * Sample file contents:

        ```python
        INSTALLED_APPS = [
            #...
            'django.contrib.admindocs',
            #...
        ]
        ```

1. Project [`Pipfile`](../Pipfile) already includes the following package dependencies:
    * `django`
    * `docutils`
    * Sample file contents:

        ```code
        #...
        [packages]
        django = "==4.1"
        docutils = "==0.19"
        #...
        ```

1. Project already has a `superuser` account created in the database.
