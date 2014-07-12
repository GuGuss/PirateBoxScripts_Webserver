PirateBox UI 2.x
================

Complete revamp of the **Piratebox UI** with additional features like extensions, translations...

**Warning**: This is still in heavy development and has not yet been tested on an actual box.

Features
--------

* Scalable artchitecture
The interface can be easily extended with extensions (chat, forum, map...).

* Responsive design
The layout is perfectly displayed on any screen size (mobile, desktop...).

* Admin UI
The admin user can log in and configure some basic stuff.

* Welcome popup
The first time the homepage loads, a popup window is displayed to explain to the user what is a Piratebox.
This could be handled as an extension.

* Multilingual interface with automatic language selection
The interface can be translated in different language and the user can choose is language.
The default language selected is the one of the user browser.

* Improved file upload
The user can upload multiple files, stop/resume an upload, drag & drop files for upload...

How to test
-----------

* Install [Flask](http://flask.pocoo.org/docs/installation/#installation)

    $ sudo apt-get update
    $ sudo apt-get install python-virtualenv

* Create the virtual environment
  
    $ cd flask
    $ virtualenv venv --distribute

* Activate the virtual environment

    $ . venv/bin/activate

* Install flask (only once)

    $ pip install Flask

* Run the python file

    $ python index.py

* Install [Babel](http://pythonhosted.org/Flask-Babel/) package for translation

    $ pip install Flask-Babel

* Export all translations

    $ pybabel extract -F babel.cfg -o messages.pot .

* Generate translation files for each language

    $ pybabel init -i messages.pot -d translations -l fr

* Compiling translations for use

    $ pybabel compile -f -d translations

* Update translations files

    $ pybabel update -i messages.pot -d translations

TODO
----

* Convertir le welcome-modal en extension
* Utiliser le JQuery File Uploader avec Python (https://github.com/blueimp/jQuery-File-Upload)
* 404 page https://bootsnipp.com/snipps/sample-404-page
* Contact page (one extension ?) https://bootsnipp.com/snipps/clean-simple-contact-form
