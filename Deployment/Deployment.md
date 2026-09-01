
IKON

Jenkins Auto deploy

UAT branch = TEST
PROD branch = master

steps
UAT/PROD deployment
1.

collation 
 sed -i 's/utf8mb4_0900_ai_ci/utf8mb4_unicode_ci/g' ikon_uat_new.sql 

run this if you are testing in upload
docker run --rm -p 3000:3000 -d gotenberg/gotenberg:7


"dump database"
dapat nasa root@Ikon-recruitment-DB

to enter root@Ikon-recruitment-DB 
root@Ikon-recruitment-DB

ssh root@139.180.191.241 -i ~/.ssh/ikon_ssh_key

%% mysqldump -uroot -pP@ssw0rd ikon_test > testdb.sql %%

dump databae in local
docker exec -i mariadb mysql -u root -p mmda > path/name.sql
EnterPassword:P@ssw0rd



run this command where do you want to save the data
ex. home or downloads open the terminal

		scp i ~/.ssh/ikon_ssh_key root@[server-ip]:[file-to-get-path] [path-to-place-in-local]
	
	example 
	
	scp -i ~/.ssh/ikon_ssh_key root@139.180.191.241:existing_command_history.sql D:\Downloads
	
scp -i ~/.ssh/ikon_ssh_key root@139.180.191.241:testdb.sql D:\Downloads
	
	"use this code in dumpdatabse in using docker"
			 docker exec -i mariadb mysqldump -h139.180.191.241 -uroot -pP@ssw0rd              ikon_test > name-of-sql.sql
		errror :
				ERROR 1273 (HY000) at line 492412: Unknown collation:                             'utf8mb4_0900_ai_ci'
		 answer
			 sed -i 's/utf8mb4_0900_ai_ci/utf8mb4_unicode_ci/g'   path-of-your-  sql-ikon_try_lang.sql
		 

	to update database in server in uat
	 you need to delete the ikon_test
	 then create a new database
	step 1
	 ken@ken-ThinkPad-L490:~$ ssh root@139.180.191.241 -i ~/.ssh/ikon_ssh_key
	 root@Ikon-Recruitment-DB:~# mysql -uroot -pP@ssw0rd ikon_test
	 mysql> Create database ikon_kenny
     mysql> use ikon_kenny;
    mysql> show tables;

	 step 2

		"use this to import database to the serve"
		run this where located in you sql file path 
			 docker exec -i mariadb mysql -h139.180.191.241 -uroot -pP@ssw0rd                  ikon_test < ikon_try_lang.sql
			 
			 
		 
		 
	 	 
	  













