# Create Django Project

1. Start in root directory of project (the directory that will contain all of project code and our `manage.py`):
    * `pwd`
    * My sample directory:

        ```console
        PS C:\Users\FlynntKnapp\Programming\02-django-admin-documentation-generator> pwd

        Path
        ----
        C:\Users\FlynntKnapp\Programming\02-django-admin-documentation-generator

        PS C:\Users\FlynntKnapp\Programming\02-django-admin-documentation-generator>
        ```

1. Create virtual environment and install Django:
    * `pipenv install django==4.1`
    * Sample console output:

        ```console
        PS C:\Users\FlynntKnapp\Programming\02-django-admin-documentation-generator> pipenv install django==4.1  
        Creating a virtualenv for this project...
        Pipfile: C:\Users\FlynntKnapp\Programming\02-django-admin-documentation-generator\Pipfile
        Using C:/Program Files/Python311/python.exe (3.11.1) to create virtualenv...
        [ ===] Creating virtual environment...created virtual environment CPython3.11.1.final.0-64 in 373ms
        creator CPython3Windows(dest=C:\Users\FlynntKnapp\.virtualenvs\02-django-admin-documentation-generator-je2EH_0z, clear=False, no_vcs_ignore=False, global=False)
        seeder FromAppData(download=False, pip=bundle, setuptools=bundle, wheel=bundle, via=copy, app_data_dir=C:\Users\FlynntKnapp\AppData\Local\pypa\virtualenv)
            added seed packages: pip==22.3.1, setuptools==65.6.3, wheel==0.38.4
        activators BashActivator,BatchActivator,FishActivator,NushellActivator,PowerShellActivator,PythonActivator
        
        Successfully created virtual environment!
        Virtualenv location: C:\Users\FlynntKnapp\.virtualenvs\02-django-admin-documentation-generator-je2EH_0z
        Creating a Pipfile for this project...
        Installing django==4.1...
        Pipfile.lock not found, creating...
        Locking [packages] dependencies...
        Locking [dev-packages] dependencies...
        Updated Pipfile.lock (ad87035279ad7566fef0860964cc374ccfb9336924ab64f936c86c7a98c92a4c)!
        Installing dependencies from Pipfile.lock (c92a4c)...
        To activate this project's virtualenv, run pipenv shell.
        Alternatively, run a command inside the virtualenv with pipenv run.
        PS C:\Users\FlynntKnapp\Programming\02-django-admin-documentation-generator>
        ```

1. Activate virtual environment:
    * `pipenv shell`
    * Sample console output:

        ```console
        PS C:\Users\FlynntKnapp\Programming\02-django-admin-documentation-generator> pipenv shell
        Launching subshell in virtual environment...
        PowerShell 7.3.1
        PS C:\Users\FlynntKnapp\Programming\02-django-admin-documentation-generator>
        ```

1. Verify that Django is installed. Note line with `Django` and line with `docutils`:
    * `pip list`
    * Sample console output:

        ```console
        PS C:\Users\FlynntKnapp\Programming\02-django-admin-documentation-generator> pip list    
        Package    Version
        ---------- -------
        asgiref    3.5.2
        Django     4.1
        pip        22.3.1
        setuptools 65.6.3
        sqlparse   0.4.3
        tzdata     2022.7
        wheel      0.38.4
        PS C:\Users\FlynntKnapp\Programming\02-django-admin-documentation-generator>
        ```

1. Create Django project:
    * `django-admin startproject config .`
    * Note: The `.` at the end of the command tells Django to create the project in the current directory.
    * Sample console output:

        ```console
        PS C:\Users\FlynntKnapp\Programming\02-django-admin-documentation-generator> django-admin startproject config .
        PS C:\Users\FlynntKnapp\Programming\02-django-admin-documentation-generator>
        ```

1. Examine conents of new Django Project directory. We will, in the future, be modifying `settings.py` and `urls.py`:
    * `tree /f /a config`:
    * Sample console output:

        ```console
        PS C:\Users\FlynntKnapp\Programming\02-django-admin-documentation-generator> tree /f /a config
        Folder PATH listing for volume Windows
        Volume serial number is 6867-B0EB
        C:\USERS\FLYNNTKNAPP\PROGRAMMING\02-DJANGO-ADMIN-DOCUMENTATION-GENERATOR\CONFIG
            asgi.py
            settings.py
            urls.py
            wsgi.py
            __init__.py
            
        No subfolders exist 

        PS C:\Users\FlynntKnapp\Programming\02-django-admin-documentation-generator>
        ```

1. Test development server:
    * Note: The development server is running on port 8000 by default.  You can change the port by adding the port number to the end of the command, e.g. `python manage.py runserver 8010`.
    * `python manage.py runserver`
    * Sample console output:

        ```console
        PS C:\Users\FlynntKnapp\Programming\02-django-admin-documentation-generator> python manage.py runserver
        Watching for file changes with StatReloader
        Performing system checks...

        System check identified no issues (0 silenced).

        You have 18 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
        Run 'python manage.py migrate' to apply them.
        December 18, 2022 - 11:19:53
        Django version 4.1, using settings 'config.settings'
        Starting development server at http://127.0.0.1:8000/
        Quit the server with CTRL-BREAK.
        ```

1. Open the development server root URL in a browser and verify the Django greeen rocket is displayed:
    * <http://localhost:8000/>
    * Sample browser image:
        ![Django Development Server](../images/django-development-server.png)
    * Sample console output:

        ```console
        [18/Dec/2022 11:20:15] "GET / HTTP/1.1" 200 10681
        ```

1. We now have a basic Django project which runs on the development server and displays a confirmation page in the browser when `DEBUG=True` in `settings.py`.  We can now start adding functionality to our project in the next section.

1. Stop the development server:
    * `Ctrl+C`

1. You can now exit the virtual environment:
    * `exit`

1. You can now run the app in the future using the following terminal commands:
    1. `pipenv shell`
    1. `python manage.py runserver`

1. You can now stop the development server in the future using the following terminal command:
    * `Ctrl+C`

1. You can now exit the virtual environment in the future using the following terminal command:
    * `exit`

1. Proceed to [Add Django AdminDocs `django.contrib.admindocs` Application](./02_add_django_admindocs.md) to add Django Admin Docs to the project.
