# User Registration Service
A microservice for allowing users to create an account for an application. 
When a registered user is authenticated, a JWT token will be returned that 
they can include in requests to access other resources.

## Requirements
In order to build and deploy this microservice you will need to have the 
following things installed:
1. Python 3.9
2. Docker
3. Openshift Cluster

## Setup
Once you have the project forked to your workstation, just run
the following commands:

```
pipenv --python 3.9
pipenv shell
pipenv install -r requirements.txt
```
## Database Migration
In order to create our database tables from the models, 
we need to use the migrateCommand through the manager 
interface. In the root of the project where manage.py 
is located, run these commands:
```
python manage.py db init
python manage.py db migrate --message 'initial database migration'
python manage.py db upgrade
```
This will create a new sqlite database in your project root.

