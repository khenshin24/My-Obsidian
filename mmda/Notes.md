dotnet ef database update --project MMDA.Backend.Core/MMDA.Backend.Core.csproj --startup-project MMDA.Backend.WebApi/MMDA.Backend.WebApi.csproj

dotnet ef migrations add candidatesite-column-change-to-nullable --project MMDA.Backend.Core/MMDA.Backend.Core.csproj --startup-project MMDA.Backend.WebApi/MMDA.Backend.WebApi.csproj

Running in Reports
dotnet watch run --project MMDA.Backend.WebApi/MMDA.Backend.WebApi.csproj 



if error in migrating check the migration file if theirs a inital 34,36,37

"INSQL null or not" 
to check the properties if it is null or not in sql
if the prop have letter v it not nullable
and if  the prop have no v value its  nullable


migrating new database
get the mmda_uat.sql import 
add migration no need to update because the database you get is already updated


CANT UPDATE DATABASE " ERROR DUPLICATE ANY TABLE"
	get press updated migration file then delete all the  file in migration folder then copy paste the migration file 
	then import the new updated database then  update the database using command

dumpdata or export data
docker exec -i mariadb mysql -uroot -pP@ssw0rd mmda > /Downloads/name.sql

mmda
sudo lsof - i :7040
kill -9 followed by number

ikon
sudo lsof - i :7015



question form add new field 













