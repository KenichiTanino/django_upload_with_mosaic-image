# django_upload_with_mosaic-image

## run

```
$ mkdir log
$ export DJANGO_SETTINGS_MODULE="django_upload.settings.production"
$ pipenv run python manage.py runserver 0.0.0.0:18889
```

## Features ##

- [Django compressor](http://django-compressor.readthedocs.org/en/latest/) to compress JS and CSS and compile LESS/SASS files.
- [Pipenv](https://docs.pipenv.org) To manage dependences and virtualenvs.
- [Django debug toolbar](http://django-debug-toolbar.readthedocs.org/) enabled for superusers.
- [Argon2](https://docs.djangoproject.com/en/2.0/topics/auth/passwords/#using-argon2-with-django) to hash the passwords

## Quickstart ##

If you need a database, edit the settings and create one with
   
    pipenv run python manage.py migrate

Once everything it's setup you can run the development server: [http://localhost:8000/](http://localhost:8000/)

    pipenv run python manage.py runserver

## How to use it ##

### Settings ###

Settings are divided by environments: production.py, development.py and testing.py. By default it uses development.py, if you want to change the environment set a environment variable:

    export DJANGO_SETTINGS_MODULE="django_upload.settings.production"

or you can use the `settings` param with runserver:

    pipenv run python manage.py runserver --settings=django_upload.settings.production

If you need to add some settings that are specific for your machine, rename the file `local_example.py` to `local_settings.py`. This file it's in .gitignore so the changes won't be tracked.
