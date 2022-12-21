# Create Django Project

1. Start in root directory of project (the directory that will contain all of project code and our `manage.py`):
    * `Get-Location`
        * An alternate command is `pwd`.
    * My sample directory:

        ```console
        PS C:\Users\FlynntKnapp\Programming\django-anonymous-user> Get-Location

        Path
        ----
        C:\Users\FlynntKnapp\Programming\django-anonymous-user

        PS C:\Users\FlynntKnapp\Programming\django-anonymous-user>
        ```

1. Get current directory contents. Note that the only files are the ones for git and GitHub:
    * The author is using a repository for this code so there are two files which may not be in your project directory. These files are the following:
        * `.gitignore`
        * `README.md`
    * `Get-ChildItem`
        * An alternate command is `ls`.
    * Sample console output:

        ```console
        PS C:\Users\FlynntKnapp\Programming\django-anonymous-user> Get-ChildItem

            Directory: C:\Users\FlynntKnapp\Programming\django-anonymous-user

        Mode                 LastWriteTime         Length Name
        ----                 -------------         ------ ----
        -a---          12/18/2022 10:22 AM           7771 .gitignore
        -a---          12/21/2022  6:26 AM            169 README.md

        PS C:\Users\FlynntKnapp\Programming\django-anonymous-user>
        ```

1. Create virtual environment and install Django:
    * `pipenv install django==4.1`
    * Sample console output:

        ```console
        PS C:\Users\FlynntKnapp\Programming\django-anonymous-user> pipenv install django==4.1
        Creating a virtualenv for this project...
        Pipfile: C:\Users\FlynntKnapp\Programming\django-anonymous-user\Pipfile
        Using C:/Program Files/Python311/python.exe (3.11.1) to create virtualenv...
        [ ===] Creating virtual environment...created virtual environment CPython3.11.1.final.0-64 in 386ms
          creator CPython3Windows(dest=C:\Users\FlynntKnapp\.virtualenvs\django-anonymous-user-VeF83pjW, clear=False, no_vcs_ignore=False, global=False)
          seeder FromAppData(download=False, pip=bundle, setuptools=bundle, wheel=bundle, via=copy, app_data_dir=C:\Users\FlynntKnapp\AppData\Local\pypa\virtualenv)
            added seed packages: pip==22.3.1, setuptools==65.6.3, wheel==0.38.4
          activators BashActivator,BatchActivator,FishActivator,NushellActivator,PowerShellActivator,PythonActivator

        Successfully created virtual environment!
        Virtualenv location: C:\Users\FlynntKnapp\.virtualenvs\django-anonymous-user-VeF83pjW
        Creating a Pipfile for this project...
        Installing django==4.1...
        Pipfile.lock not found, creating...
        Locking [packages] dependencies...
        Locking [dev-packages] dependencies...
        Updated Pipfile.lock (c9c7d544ca3f1abd9c77a7a700900f8ac14c62a62f0860454fd1e5e7d9c21913)!
        Installing dependencies from Pipfile.lock (c21913)...
        To activate this project's virtualenv, run pipenv shell.
        Alternatively, run a command inside the virtualenv with pipenv run.
        PS C:\Users\FlynntKnapp\Programming\django-anonymous-user>
        ```

1. Examine current directory contents:
    * `Get-ChildItem`
        * An alternate command is `ls`.
    * The following two files should have been added to your directory:
        * `Pipfile`
        * `Pipfile.lock`
    * Sample console output:
    * The actual files which will are contained in the virtual environment are not in the project directory. They are usually in a directory named `.venv` or `.virtualenvs` in your home directory.
        * Location for this project's virtual environment are noted in the console output above by line with `Virtualenv location`:
            * Virtualenv location: C:\Users\FlynntKnapp\.virtualenvs\django-admin-documentation-generator-BFISvjYE
    * These files are used by `pipenv` to manage the virtual environment and it's package dependencies.

        ```console
        PS C:\Users\FlynntKnapp\Programming\django-anonymous-user> Get-ChildItem

            Directory: C:\Users\FlynntKnapp\Programming\django-anonymous-user

        Mode                 LastWriteTime         Length Name
        ----                 -------------         ------ ----
        -a---          12/18/2022 10:22 AM           7771 .gitignore
        -a---          12/21/2022  6:50 AM            156 Pipfile
        -a---          12/21/2022  6:50 AM           1775 Pipfile.lock
        -a---          12/21/2022  6:26 AM            169 README.md

        PS C:\Users\FlynntKnapp\Programming\django-anonymous-user>
        ```

1. Activate virtual environment:
    * `pipenv shell`
    * This command doesn't add any files to the project directory, it just activates the virtual environment so the project python files can use the packages installed in the virtual environment.
    * Sample console output:

        ```console
        PS C:\Users\FlynntKnapp\Programming\django-anonymous-user> pipenv shell
        Launching subshell in virtual environment...
        PowerShell 7.3.1
        PS C:\Users\FlynntKnapp\Programming\django-anonymous-user>
        ```

1. Verify that Django is installed. Note line with `Django`:
    * `pip list`
    * Sample console output:

        ```console
        PS C:\Users\FlynntKnapp\Programming\django-anonymous-user> pip list
        Package    Version
        ---------- -------
        asgiref    3.6.0
        Django     4.1
        pip        22.3.1
        setuptools 65.6.3
        sqlparse   0.4.3
        tzdata     2022.7
        wheel      0.38.4
        PS C:\Users\FlynntKnapp\Programming\django-anonymous-user>
        ```

1. Create Django project:
    * `django-admin startproject config .`
    * Note: The `.` at the end of the command tells Django to create the project in the current directory.
    * Sample console output:

        ```console
        PS C:\Users\FlynntKnapp\Programming\django-anonymous-user> django-admin startproject config .
        PS C:\Users\FlynntKnapp\Programming\django-anonymous-user>
        ```

1. Examine current directory contents:
    * `Get-ChildItem`
        * An alternate command is `ls`.
    * The following directory and file should have been added to your directory:
        * `config`
        * `manage.py`
    * The `config` directory contains the Django project files.
    * The `manage.py` file is used to manage the Django project.
    * Sample console output:

        ```console
        PS C:\Users\FlynntKnapp\Programming\django-anonymous-user> Get-ChildItem

            Directory: C:\Users\FlynntKnapp\Programming\django-anonymous-user

        Mode                 LastWriteTime         Length Name
        ----                 -------------         ------ ----
        d----          12/21/2022  6:56 AM                config
        -a---          12/18/2022 10:22 AM           7771 .gitignore
        -a---          12/21/2022  6:56 AM            684 manage.py
        -a---          12/21/2022  6:50 AM            156 Pipfile
        -a---          12/21/2022  6:50 AM           1775 Pipfile.lock
        -a---          12/21/2022  6:26 AM            169 README.md

        PS C:\Users\FlynntKnapp\Programming\django-anonymous-user>
        ```

1. Examine contents of new Django Project directory [`config`](../config/) . We will, in the future, be modifying [`config/settings.py`](../config/settings.py) and [`urls.py`](../config/urls.py) files:
    * `Get-ChildItem config`:
        * An alternate command is `ls config`.
    * Sample console output:

        ```console
        PS C:\Users\FlynntKnapp\Programming\django-anonymous-user> Get-ChildItem config

            Directory: C:\Users\FlynntKnapp\Programming\django-anonymous-user\config

        Mode                 LastWriteTime         Length Name
        ----                 -------------         ------ ----
        -a---          12/21/2022  6:56 AM              0 __init__.py
        -a---          12/21/2022  6:56 AM            405 asgi.py
        -a---          12/21/2022  6:56 AM           3342 settings.py
        -a---          12/21/2022  6:56 AM            769 urls.py
        -a---          12/21/2022  6:56 AM            405 wsgi.py

        PS C:\Users\FlynntKnapp\Programming\django-anonymous-user>
        ```

1. Test development server:
    * `python manage.py runserver`
    * Sample console output:

        ```console
        PS C:\Users\FlynntKnapp\Programming\django-anonymous-user> python manage.py runserver
        Watching for file changes with StatReloader
        Performing system checks...

        System check identified no issues (0 silenced).

        You have 18 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
        Run 'python manage.py migrate' to apply them.
        December 21, 2022 - 06:59:50
        Django version 4.1, using settings 'config.settings'
        Starting development server at http://127.0.0.1:8000/
        Quit the server with CTRL-BREAK.
        ```

    * Note: The development server is running on port 8000 by default.  You can change the port by adding the port number to the end of the command, e.g. `python manage.py runserver 8010`.

1. Open the development server root URL in a browser and verify the Django greeen rocket is displayed:
    * <http://localhost:8000/>
    * Sample browser image:
        ![Django Development Server](../images/django-development-server.png)
    * Relevant sample console output:

        ```console
        ...
        [18/Dec/2022 10:58:34] "GET / HTTP/1.1" 200 10681
        ...
        ```

1. We now have a basic Django project which runs on the development server and displays a confirmation page in the browser when `DEBUG=True` in `settings.py`.  We can now start adding functionality to our project in the next section.

1. Stop the development server:
    * `Ctrl+C`

1. You can now exit the virtual environment:
    * `exit`

1. You can now run the app in the future using the following terminal commands and link:
    1. `pipenv shell`
        * Activates the virtual environment.
    1. `python manage.py runserver`
        * Starts the development server.
    1. <http://localhost:8000/>
        * Opens the development server root URL in a browser.
    1. `Ctrl+C`
        * Stops the development server.
    1. `exit`
        * Exits the virtual environment.

1. Continue on to [Add Django AdminDocs (`django.contrib.admindocs`) Application](./02_add_django_admindocs.md).

    * We will add the [Django Documentation Generator](https://docs.djangoproject.com/en/4.1/ref/contrib/admin/admindocs/#module-django.contrib.admindocs) in the next section. This will allow us to generate documentation for our project and view existing documentation provided by Django.

## Repository Links

* [django-03-anonymous-user](https://github.com/FlynntKnapp/django-03-anonymous-user)
* [django-03-anonymous-user - `README.md`](https://github.com/FlynntKnapp/django-03-anonymous-user/blob/main/README.md)
