# Useful-Repetitive-Commands
List of useful &amp; repetitive commands & file structures in various different technologies 
<br/>
<br/>
## Git
### Initialize Git Repository in VS Code
Ctrl+Shift+P and enter Git: Clone (add repository URL) + Fetch/Pull
<br/>
<br/>
`git checkout -b new-branch-name existing-branch-name`
<br/>
<br/>
## Python - Snowflake
### .env Structure for VS Code when Connecting to the Account 
```
user=user
password=password
account=account
warehouse=warehouse
database=database
schema=schema
```
### Connect the credentials
```
import snowflake.connector
import os

from dotenv import load_dotenv

load_dotenv() 

conn = snowflake.connector.connect(
    user=os.getenv("user"),
    password=os.getenv("password"),
    account=os.getenv("account"),
    warehouse=os.getenv("warehouse"),
    database=os.getenv("database"),
    schema=os.getenv("schema")
)
```
## dbt + VS code extension
`pip install dbt-core dbt-Snowflake` 
<br/>
`dbt init <project_name> (Initialize project in VS code, use underscore)`
<br/>
`dbt run` (E2E)
<br/>
`dbt show --select stg_transactions__pdf_transaction_view` (Show query results from model run)
<br/>
`dbt clean`
## Django
`.env` needs to be in same folder as `manage.py`
<br/>
<br/>
`python manage.py runserver`
<br/>
<br/>
`django-admin startproject my_tennis_club` (Create project)
<br/>
<br/>
`python manage.py startapp members` (Create the app after navigating to project folder)
<br/>
<br/>
Migrations:
<br/>
`python manage.py makemigrations`
<br/>
<br/>
`python manage.py migrate`
## MySQL
Method 2: Windows Background Services
<br/>
<br/>
If the menu options inside Workbench are grayed out or throw a connection failure error, the local Windows background service is turned off.
1. Press Win + R, type services.msc, and hit Enter.
2. Scroll down to find MySQL (usually labeled MySQL80 or MySQL90).
3. Right-click the service and select Start.
