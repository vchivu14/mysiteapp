=====
Users
=====

Users is a Django app to create profiles and provide login.

Detailed documentation is in the "docs" directory.

Quick start
-----------

1. Add "users" to your INSTALLED_APPS setting like this::

    INSTALLED_APPS = [
        ...
        'crispy_forms',
        'users.apps.UsersConfig',
    ]

    Create a folder name "media" inside your projects folder, the one with manage.py

2. Read the settings.txt from inside the 'users' folder, 
    there are two paragraphs which need to be added to
    your project settings file.
    - The Fist paragraph(Settings File) needs to be attached
        at the bottom of your settings.py file;
    - The Second paragraph(Settings File) needs to be attached,
        along with the others urls you may have and make changes
        if path names collide.

3. Create a virtual envvironment if possible, and install 
    the requirements from inside the 'users' folder
$ pip install -r requirements txt
Then come back to the main folder the one that has the 'users-app' folder 
    and install the users app:
$ pip install users-app/dist/users-app-0.1.tar.gz

4. Make migrations:
$ python3 manage.py makemigrations
Apply migrations:
$ python3 manage.py migrate

4. (*OPTIONAL STEP)
    Create your config.json file in your envvironment with credentials so you can use mail retrieval.
    (the project has a default location from where it loads the file
    "/etc/config.json", like it's stated in the settings file,
    you can use that or place it in another location and add the credentials required
    in key-value pairs like {'EMAIL_USER':"your email", 'EMAIL_PASS':"your passwd"}).
    (!!!DON'T SHARE THIS WITH ANYONE, KEEP IT SAFE ONLY ON YOUR ENVIRONMENT)

5. Start the development server and visit http://127.0.0.1:8000/login/
   to check everything worked out, and register a new user.

6. Link the user to other parts of your app...
