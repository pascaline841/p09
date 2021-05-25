<h1 align="center">DJANGO Project -  LIT REVIEW  -  OpenClassRooms Project 09 </h1><br>
<br>
Ce script Python est le neuvieme projet réalisé dans le cadre d'une formation chez OpenClassrooms. 
<br>
  
## OVERVIEW
Beta version of a website made with Django. Allows you to post reviews to respond to the reviews of other user, to post your own review and to follow users and their posts.
<br>


## REQUISITORIES 
Python3<br>
asgiref==3.3.4<br>
Django==3.2.2<br>
Pillow==8.2.0<br>
psycopg2==2.8.6<br>
pytz==2021.1<br>
sqlparse==0.4.1<br>
<br>

## INSTALLATION 

Start by closing the repository :

```
git clone https://github.com/pascaline841/p9
```
- Start access the project folder

- Create a virtual environment
```
python -m venv venv
```
- Enable the virtual environment 
```
cd venv/scripts
```
```
source activate
```
- Install the python dependencies on the virtual environment
```
pip install -r requirements.txt
```
- Instal PostgreSQL
https://www.postgresql.org/

- Launch SQL Shell to create a user and a database :
```
psql
CREATE USER admin WITH ENCRYPTED PASSWORD 'OCPython2021';
ALTER ROLE admin SET client_encoding TO 'utf8';
ALTER ROLE admin SET default_transaction_isolation TO 'read_committed';
CREATE DATABASE litreview;
GRANT ALL PRIVILEGES ON DATABASE litreview TO admin;
```
- Leave the SQL Shell 
- Migrate the data structures to the database and test out the server.
```
python manage.py makemigrations
python manage.py migrate
```
After creating the database structure, create an administrative account by typing:
```
python manage.py createsuperuser
```
You will be asked to select a username, provide an email address, and choose and confirm a password for the account.

## LAUNCH 

Run the program
```
python manage.py runserver
```
Launch
```
http://127.0.0.1:8000
```
