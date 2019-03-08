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
    workon venv

    ## to deativate the venv
    deativate       

$ workon flaskr
$ pip install wheel
$ pip install flaskr-1.0.0-py3-none-any.whl

## activate database
$ export FLASK_APP=flaskr
$ flask init-db

## set up web app and wsgi file
$ ???
$ ???



TODO
- check and see why pytest is not running? may have something to do with the file location of setup.cfg? or may have something to do with what directory you are in when you run $ pytest from the CLI ? http://flask.pocoo.org/docs/1.0/tutorial/tests/
