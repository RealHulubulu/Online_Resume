# Python Django app to display a resume

This is a barebones Django app, which can easily be deployed to Heroku. I've take the tutorial on Heroku's website and made it into something more practical.
You have to input the correct resume data into the index.html file. To change the colors adjust the values in the base.html file. There is a database attached 
to this app that just keeps track of when the site is visited.

This app is built using the [Getting Started with Python on Heroku](https://devcenter.heroku.com/articles/getting-started-with-python) article - check it out. 
The tutorial above will help if you get stuck trying to deploy your own app.

## Running Locally

Make sure you have Python 3.7 [installed locally](http://install.python-guide.org). To push to Heroku, you'll need to install the [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli), as well as [Postgres](https://devcenter.heroku.com/articles/heroku-postgresql#local-setup).

```sh
$ git clone https://github.com/RealHulubulu/Online_Resume.git

$ python3 -m venv new_venv
$ pip install -r requirements.txt

$ createdb 

$ python manage.py migrate
$ python manage.py collectstatic

$ heroku local
```

Your app should now be running on [localhost:5000](http://localhost:5000/).

## Deploying to Heroku

```sh
$ heroku create
$ git push heroku master

$ heroku run python manage.py migrate
$ heroku open
```
or

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

## Documentation

For more information about using Python on Heroku, see these Dev Center articles:

- [Python on Heroku](https://devcenter.heroku.com/categories/python)
