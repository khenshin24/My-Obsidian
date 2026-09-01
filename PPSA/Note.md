	.venv\Scripts\activate
app.py as program cs

after you delete the table if you want to delete the table you shoud delete the file of migrations

to run the application flask run

models
		model
		ex . noticemodel 
			after reg to init.py
					migrate = flask db init
								flask db migrate
										flask db upgrade
schemas
		 like required string length
resources
		api controller
register
			app.py   register the api controller
create factory
			in model

swagger
		open
			host - swagger-ui
to have venv
    python -m venv .venv
    PS C:\Users\custo\repo\PPSA.Identity.API> .venv\Scripts\activate
	cmd  venv/bin/activate

	use the username postgres
		     psql -U postgres

	postgre Password
			kenny123
			
	Create database 
	CREATE DATABASE ppsa;
	 outoput to message to successfully created a database 'CREATE DATABASE'

	list all the databse in \l
	 Create database connection in the dbeave name the database is ppsa
	 
		then \c ppsa 
			 to connect to the database
		then \i  
		ppsa=# \i c:/path/path/data/data01.sql
		i is to import your database
		 NOTE "possible error denied if the "'\' is like this"
	

	importing databse in postgres 
	https://stackoverflow.com/questions/3204274/importing-sql-file-on-windows-to-postgresql

pip install flask -smorest
pip install Flask-JWT-Extended
pip install Flask-Mail
pip install passlib
pip install psycopg2-binary


DATABASE_URL=postgresql://postgres:kenny123@localhost:5432/ppsa_identity_dev

https://www.postgresql.org/download/linux/debian/


execution policy
Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

Install the latest PowerShell for new features and improvements! https://aka.ms/PSWindows

PS C:\Windows\system32> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine

Execution Policy Change
The execution policy helps protect you from scripts that you do not trust. Changing the execution policy might expose
you to the security risks described in the about_Execution_Policies help topic at
https:/go.microsoft.com/fwlink/?LinkID=135170. Do you want to change the execution policy?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): a
PS C:\Windows\system32> get-executionpolicy
RemoteSigned
PS C:\Windows\system32>



Delete Database in PSQL
### **Step 1: Connect to PostgreSQL**

Open your terminal or command prompt and connect to PostgreSQL using:

`psql -U your_username`

Replace `your_username` with your PostgreSQL username.

### **Step 2: Disconnect from the Database**

You cannot drop a database while you are connected to it. First, switch to the default `postgres` database or any other database:

`\c postgres;`

### **Step 3: Drop the Database**

Run the following command to delete the database:

`DROP DATABASE your_database_name;`

Replace `your_database_name` with the name of the database you want to delete.

### **Step 4: Verify Deletion**

You can list all databases to confirm the deletion:

`\l`

