# ibm
open git bash
```sh
cd ~/Documents/scripts

./pfis-ssh-ibm.sh

./ssh-web.sh

#to activate bash type 
bash


cd repos/PFIS.Server.Files/
./restore_ibm.sh

# enter
DOTUAT.sql
```
    
  
# Test Server
	wire guard
	 pfis activate
    cd ~/Documents/scripts
	./pfis-db-dotuat-restore.sh
	DOTUAT.sql





psql -h localhost -d pfis -f TRIGGERS.sql
psql -U postgres -h localhost -d dbname -f TRIGGERS.sql
		 



      
      
      
