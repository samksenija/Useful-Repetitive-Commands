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
`user=user`<br/>
`password=password`<br/>
`account=account`<br/>
`warehouse=warehouse`<br/>
`database=database`<br/>
`schema=schema`<br/>
### Connect the credentials
`import snowflake.connector`<br/>
`import os`<br/>
<br/>
`from dotenv import load_dotenv`<br/>
<br/>
`load_dotenv() `<br/>
<br/>
`conn = snowflake.connector.connect(`<br/>
`    user=os.getenv("user"),`<br/>
`    password=os.getenv("password"),`<br/>
`    account=os.getenv("account"),`<br/>
`    warehouse=os.getenv("warehouse"),`<br/>
`    database=os.getenv("database"),`<br/>
`    schema=os.getenv("schema")`<br/>
`)`
