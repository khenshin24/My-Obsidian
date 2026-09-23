
	AKS first kung may nag TETEST

- Git pull all branch in trello 
	- `git pull origin branch`
	- All branches merge to uat-findings-2

	Database in DEV > DOTUAT > PROD
	 Same Same lang yan sila Meaning Sa DEV pag mag papadeploy sa DOTUAT and PROD
			copy the DEV.sql then Rename as DOTUAT and PROD

- Database Change
	- Backup Current Database
		- git terminal cmd pfis-db-backup.sh
	- Reset Database
		- git terminal cmd pfis-db-reset.sh
	- Build Backend
		- `npm run clean`
		- `npm run build`
		- npm run dev
			- this will create tables 
		- run triggers
			- inside the project
			- `psql -h localhost -U postgres -d pfis_1 -f TRIGGERS.sql`
		- npm run dev
			- Seed Masterfiles
		- Backup Database have No uat-findings-2 branch only DEV-DOTUAT-PROD
		- DEV branch
		- git terminal cmd pfis-db-backup.sh
			- save as DEV.sql
			- Move the tmp/DEV.sql file to PFIS.Server.Files
		- commit and push

	
	pull changes from uat-findings-2 to DEV branch then git push


Reset-Database
	github
	 PFIS-Server-Files
		- `Action`
		- `DEV`
		- `Run work flow`
		- `DEV`
		- `Deploy`

uat-findings-2 > DEV > DOTUAT > PROD

DOTUAT branch Deploys both to IBM and UAT

	DOTUAT -> git pull origin DEV
	 Backend
	 Web
	 Database
	 
	git pull
		git pull origin DEV
			git push
	
	database conflict 
		accept all incoming

deploy PROD
	branch PROD > git pull DOTUAT
	 backend
	 web
	 database



commit Message "updated

