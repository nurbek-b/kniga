
### To run this project:
* Clone this repository
```
git clone git@github.com:NurbekAka/kniga.git
```

* Activate virtual environment:
```
pip install pipenv
pipenv --python 3
pipenv shell
pipenv install
```

* Create private `.env` file inside of project directory. Copy all data from `.env_example` and paste inside of `.env` file. **Note**: Change the values of secrets to yours. 

* This project uses Postgresql, so, create Postgresql database:
```
sudo apt-get update
sudo apt-get install python3-pip python3-dev libpq-dev postgres postgres-contrib
sudo su - postgres
```
* Enter postgres console:
```
psql
CREATE DATABASE db_name;
CREATE USER ashar_user WITH PASSWORD 'your_super_secret_password';
ALTER ROLE your_user SET client_encoding TO 'utf8';
ALTER ROLE your_user SET default_transaction_isolation TO 'read committed';
ALTER ROLE your_user SET timezone TO 'UTC';
GRANT ALL PRIVILEGES ON DATABASE ashar TO 'your_user';
```


* Finally, run project with command: `python3 manage.py runserver`
