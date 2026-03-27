# Useful-Repetitive-Commands
List of useful &amp; repetitive commands & file structures in various different technologies 
<br/>
<br/>
## Git
### Initialize Git Repository in VS Code
Ctrl+Shift+P and enter Git: Clone (add repository URL) + Fetch/Pull
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
