


<ol>
  <li>
  Add "users" to your INSTALLED_APPS setting like this:
  INSTALLED_APPS = [
    ...
    'crispy_forms',
    'users.apps.UsersConfig',
  ]
  </li>
  <li>cd blogapp</li>
  <li>python3 -m venv venv</li>
  <li>source venv/bin/activate</li>
  <li>pip install -r requirements.txt</li>
  <li>python3 manage.py migrate</li>
  <li>python3 manage.py createsuperuser</li>
  <li>python3 manage.py runserver</li>
  <li>check localhost:8000</li>
</ol>
<h5> Create a file named config.json on your computer with credentials to enable mail retrieval</h5>
<ul>
  <li>$ sudo nano /etc/config.json</li>
  <li># paste in your own credentials just like bellow</li>
  <li>{
        "EMAIL_USER": "",
        "EMAIL_PASS": ""
    }</li>
</ul>
<h5>Don't share this file with anyone</h5>

<h5>And thanks to Corey Schaffer for his tutorial, which helped me build this app</h5>



=====
Users
=====

Users is a Django app to create profiles and provide login.

Quick start
-----------

<ol>
    <li>Add "users" to your INSTALLED_APPS setting like this:

    INSTALLED_APPS = [
        ...
        'crispy_forms',
        'users.apps.UsersConfig',
    ]
    </li>
    
    <li>
    Create a folder name "media" inside your projects folder, the one with manage.py
    </li>

    <li>Read the settings.txt from inside the 'users' folder, there are two paragraphs which need to be added to your project settings file.
    <ul>
        <li>The Fist paragraph("""Settings File""") needs to be attached at the bottom of your settings.py file</li>
        <li>The Second paragraph("""Urls File""") needs to be attached, along with the others urls in your urls.py file (make changes if path names collide)</li>
    </ul>
    </li>

    <li>Create a virtual envvironment if possible, and install  the requirements from inside the 'users' folder: 
    $ pip install -r requirements txt
    Then come back to the main folder the one that has the 'users-app' folder and install the users app:
    $ pip install users-app/dist/users-app-0.1.tar.gz
    </li>

    <li>Make migrations:
    $ python3 manage.py makemigrations
    Apply migrations:
    $ python3 manage.py migrate
    </li>

    <li>(*OPTIONAL STEP)
    Create your config.json file in your envvironment with credentials so you can use mail retrieval.
    (the project has a default location from where it loads the file "/etc/config.json", like it's stated in the settings file.
    You can use that or place it in another location and add the credentials required in key-value pairs like {'EMAIL_USER':"your email", 'EMAIL_PASS':"your passwd"}).
    (!!!DON'T SHARE THIS WITH ANYONE, KEEP IT SAFE ONLY ON YOUR ENVIRONMENT)
    </li>

    <li>Start the development server and visit http://127.0.0.1:8000/login/ to check everything worked out, and register a new user.</li>

    <li>Link the user to other parts of your app...</li>
 </ol>
