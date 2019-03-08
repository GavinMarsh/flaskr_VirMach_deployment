# flaskr

## Activating flask server:

export FLASK_APP=flaskr
export FLASK_ENV=development
flask run


## local - Initialise the database
flask init-db

## pythonanywhere - build & install
Upload installation wheel file to files folder.
$ mkvirtualenv flaskr --python=/usr/bin/python3.7

    commands for venv:
    ## to activate the venv
    $ workon flaskr

    ## to deativate the venv
    $ deativate       

$ workon flaskr
$ pip install wheel
$ pip install flaskr-1.0.0-py3-none-any.whl

## activate database
$ export FLASK_APP=flaskr
$ flask init-db

## set up web app and wsgi file
create a new file called run.py in the flaskr source code directory (same directory where the
static & templates folders are located.

    ## run.py
    import os

    from flaskr import create_app
    from flask import Flask

    app = create_app()

In the wsgi file write:

    ## wsgi_file.py
    import sys

    # add your project directory to the sys.path
    project_home = u'/home/GMM/flaskr/'
    if project_home not in sys.path:
        sys.path = [project_home] + sys.path

    # You can't import a variable that is local to a function, so we need to call
    # the function inside the application-factory to buid and return the app.

    from flaskr import create_app
    application = create_app()



TODO
- check and see why pytest is not running? may have something to do with the file location of setup.cfg? or may have something to do with what directory you are in when you run $ pytest from the CLI ? http://flask.pocoo.org/docs/1.0/tutorial/tests/
