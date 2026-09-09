
- Git pull all branch in trello 
	- `git pull origin branch`
	- All branches merge to uat-findings-2

- Database Change
	- Backup Current Database
	- Reset Database
	- Build Backend
		- `npm run clean`
		- `npm run build`
		- npm run dev
			- this will create tables 
		- run triggers
			- `psql -h localhost -U postgres -d pfis_1 -f TRIGGERS.sql`
		- npm run dev
			- Seed Masterfiles
		- Backup Database
			- save as DEV.sql
			- make sure Dev branch
			- Move the tmp/DEV.sql file
		- commit and push

	
	pull changes from uat-findings-2 to DEV branch