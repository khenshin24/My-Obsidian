
bun install 

install it inside the project
	-c "irm bun.sh/install.ps1|iex"

run bun
	bun run dev

NBI Process
	Entity -> reg. index.ts -> 
		run migration 
			Generate Migration
			 bunx drizzle-kit generate --name=name_of_the_migration  
			Apply Migration
			 bunx drizzle-kit push
	
	
	Service
	DTO
	Controller

pg_dump -U username -h localhost -d databasename --schema-only > filename.sql




db.insert
db.select
db.update
db.delete


Re migrate
delete database
delete all files in drizzle/meta except _journal
	bunx drizzle-kit generate --name=init
	bunx drizzle-kit push
		run trigger 
			psql -U postgres -h localhost -d nbi -f C:\Users\acer\repo\nbi\NBI.ECPIS.Backend\TRIGGERS.sql


Run Worker
		bun run workerWindows 
		

----------------------------------------------
Schema -> Drizzel

Route
Controller
Service
Entity


WEB


menu.ts
