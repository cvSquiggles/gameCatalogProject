# Game catalog website

This is a Python3 project using the flask framework to build a simple **CRUD** functional website.

The homepage displays the list of all available genres, and from there,
users can navigate to each genre and **READ** all of the games within those genres.

Games can be clicked to reveal various details about the game.

**If a user is logged in** via the login button, they are able to **CREATE** new games
within each genre. They can also **UPDATE/DELETE** games that they created themselves.

It connects to the *gameCatalog.db* file to store user info, game info, and genre info.
It also utlitizes Google Oauthorization in order to handle user credentials.

The css/front-end isn't stylized yet, as focus of project was on CRUD functionality with the flask framework.
(*Project **will** be updated with better styling!*)

The google Oauth code is borrowed from a fellow students response on how to modernize the
old code that Udacity's Full-stack program suggests using. 
A helpful explanation can be found [here](https://developers.google.com/identity/sign-in/web/server-side-flow).


## Requirements
```
bleach==3.1.0
certifi==2019.3.9
chardet==3.0.4
Click==7.0
Flask==1.0.3
Flask-HTTPAuth==3.3.0
Flask-SQLAlchemy==2.4.0
httplib2==0.13.0
idna==2.8
itsdangerous==1.1.0
Jinja2==2.10.1
MarkupSafe==1.1.1
oauth2client==4.1.3
packaging==19.0
passlib==1.7.1
psycopg2-binary==2.8.2
pyasn1==0.4.5
pyasn1-modules==0.2.5
pyparsing==2.4.0
redis==3.2.1
requests==2.22.0
rsa==4.0
six==1.12.0
SQLAlchemy==1.3.4
urllib3==1.25.3
webencodings==0.5.1
Werkzeug==0.15.4
```

## How to run

1. First make sure your server has all necessary dependencies listed above, and install or update them as necessary.

2. Simply place the file on your updated server, and run the *project.py* file to begin.

3. By default the host is localhost, and the port is 5000. Change these accordingly at the bottom of the *project.py* file in app.run()

4. If you would like to start from scratch with the database, you can delete the *gamecatalog.db* file, and run the *db_setup.py* file to get an empty database.
   You can then use *dbPop.py* to populate the databse with games or genres of your choice.

#### Heads up on adding new genres to the site!

There is no way to **CREATE** new genres through the websites' functionality, this must be done through dbPop.py manually.
**THIS IS INTENTIONAL** as letting users create genres was determined to be too messy and confusing.

Genres can be very arbitrary, and without a preset structure for genres, things quickly became disorganized.