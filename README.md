# REST API using Flask-RestPlus

## Table of contents

- [About](#about)
- [How to run the application?](#how-to-run-the-application)

## About

REST API using Flask-RestPlus

This code uses the SQLite3 (https://www.sqlite.org/index.html) database to store users.

The user table has the following fields:

- **id** unique identifier for users. Numeric type.
- **email** email. String type. Should be unique and not nullable.
- **registered_on** registered date. DateTime type. Should be not nullable.
- **admin** level of access. Boolean type. Should be not nullable and has default value equals False.
- **public_id** public id. String type. Should be unique.
- **username** username. String type. Should be unique.
- **password_hash** password_hash. String type.

User operations:

* Creating a new user
* Getting a registered user with his public_id
* Getting all registered users.

**User Service class:** This class handles all the logic relating to the user model.

**User Controller:** The user controller class handles all the incoming HTTP requests relating to the user.

## How to run the application

1. Install [virtualenv](https://virtualenv.pypa.io/en/latest/) and activate the virtual environment.
	* To activate the virtualenv on Linux or MacOS: ```source venv/bin/activate```
	* To activate the virtualenv on Windows: ```\venv\Script\activate.bat```

2. Run the application

Step-by-step:

```sh
cd FlaskRestPlusTest/

virtualenv venv

source venv/bin/activate

pip install -r requirements.txt

python manage.py runserver
```

**Note**: To desactivate the virtual environment

```sh
deactivate
```